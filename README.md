# my sketch for 2019 test

# Elastic Beanstalk 
Deployment modes:
- All at Once - probably only suitable for dev. all ec2 are down during this time
- Rolling update - perf impact, instances will be down during deployment, and roll-back required another depolyment
- Rolling with additional batch - no perf impact, but requires another deployment for roll-back
- Immutable  - preferred for mission critical system, a new ec2 fleet is created and switch over to the new scaling group upon successful execution

.ebextensions
yml or json files for configs with .config extension

RDS
Dev: recommend to lauch RDS within EBS
Prod: Not recommended to launch RDS within EBS as termination of EBS will auto terminate RDS. Recommend launch RDS in solo, attach sec group and connection string to EBS

