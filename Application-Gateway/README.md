### Application Gateway Template Descriptions ###

Deployment Method:
This GIT folder is where all the Application Gateway templates will live. The engineers creating new Application Gateway should copy the template file and parameter file to individual Prod and Dev Application Gateway folders under each subscription. Normally you can have only one template file and multiple parameters file for each Application Gateway.

Please note that App Gateway supports SSL cerficiates only in pfx format.

**Exteranal App Gateway Template List:**

1. **external-appgw-https** - This template creates an External AppGW with WAF disabled, one backend pool, one Rule, FrontEnd port 443 and backend port ANY and no HealthProbe URL. The backend VMs can be added by developer teams using the resource ID of the AppGW BackendPool.
`Parameters:
Backend Pool - One,
Rule - One,
FrontEnd Port - HTTPS,
BackEend Port - ANY,
Health Probe - None
WAF - Disabled`


2. **external-appgw-dual-http-https** - This template creates an External AppGW with WAF disabled, one backend pool, one Rule, FrontEnd port 443 and backend port ANY and no HealthProbe URL. The backend VMs can be added by developer teams using the resource ID of the AppGW BackendPool.
`Parameters:
Backend Pool - One,
Rule - One,
FrontEnd Port - HTTPS,
BackEend Port - ANY,
Health Probe - None
WAF - Disabled`


3. **external-appgw-dual-http-https-customprobe** - This template creates an External AppGW with WAF disabled, one backend pool, two Rules, FrontEnd port 80 and 443 and backend ports ANY with a custom HealthProbe URL for frontend ports. The backend VMs can be added by developer teams using the resource ID of the AppGW BackendPool.
`Parameters:
Backend Pool - One,
Rule - Two,
FrontEnd Port - HTTP & HTTPS,
BackEend Port - ANY,
Health Probe - Custom
WAF - Disabled`

**Internal App Gateway Template List:**

1. **internal-appgw-http** - This template creates an Internal AppGW with WAF disabled, one backend pool, one Rule, FrontEnd port 80 and backend port ANY and no HealthProbe URL. The backend VMs can be added by developer teams using the resource ID of the AppGW BackendPool.
`Parameters:
Backend Pool - One,
Rule - One,
FrontEnd Port - HTTP,
BackEend Port - ANY,
Health Probe - None
WAF - Disabled`


2. **internal-appgw-https** - This template creates an Internal AppGW with WAF disabled, one backend pool, one Rule, FrontEnd port 443 and backend port ANY and no HealthProbe URL. The backend VMs can be added by developer teams using the resource ID of the AppGW BackendPool.
`Parameters:
Backend Pool - One,
Rule - One,
FrontEnd Port - HTTPS,
BackEend Port - ANY,
Health Probe - None
WAF - Disabled`
