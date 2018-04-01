### Load Balancer Template Descriptions ###

Deployment Method:
This GIT folder is where all the Load Balancer templates will live. The engineers creating new Load Balancers should copy the template file and parameter file to individual Prod and Dev Load Balancer folders under each subscription. Normally you can have only one template file and multiple parameters file for each Load Balancer.

**Exteranal Load Balancer Template List:**

1. **external-lb-httpprobe** - This template creates an External LB with a single Backend Pool, one Load Balancing Rule, FrontEnd and BackEnd ports set to 80 and HealthProbe URL can be set to a custom URL. The backend VMs can be added by developer teams using the resource ID of the Load Balancer BackendPool.
`Parameters:
Backend Pool - One,
LB Rule - One,
FrontEnd Port - HTTP,
BackEend Port - HTTP,
Health Probe - HTTP Custom URL`

2. **external-lb-tcpprobe** - This template creates an External LB with a single Backend Pool, one Load Balancing Rule, FrontEnd and BackEnd ports that can be configured to any port numbers and no HealthProbe URL (only TCP probe). The backend VMs can be added by developer teams using the resource ID of the Load Balancers Backend Pool.
`Parameters:
Backend Pool - One,
LB Rule - One,
FrontEnd Port - Any TCP port,
BackEend Port - Any TCP port,
Health Probe - TCP probe`

3. **external-lb-singlepool-dualport-httptcp-singleprobe** - This template creates an External LB with a single Backend Pool, two Load Balancing Rules, two FrontEnd and BackEnd ports with one port as port 80 with a Custom HealthProbe URL and second port as any TCP port with TCP probe (no HealthProbe URL). The backend VMs can be added by developer teams using the resource ID of the Load Balancers Backend Pool.
`Parameters:
Backend Pool - One,
LB Rule - Two,
FrontEnd Ports - HTTP and any TCP port,
BackEend Ports - HTTP and any TCP port,
Health Probe - Custom URL HTTP Probe for HTTP port and TCP probe for TCP port`

4. **external-lb-singlepool-dualport-httptcp-dualhttpprobe** - This template creates an External LB with a single Backend Pool, two Load Balancing Rules, two FrontEnd and BackEnd ports and a HTTP Probe with Custom URL on both the ports. The backend VMs can be added by developer teams using the resource ID of the Load Balancers Backend Pool.
`Parameters:
Backend Pool - One,
LB Rule - Two,
FrontEnd Ports - HTTP and any TCP port,
BackEend Ports - HTTP and any TCP port,
Health Probe - Custom URL HTTP Probe for both the ports.`

**Internal Load Balancer Template List:**

1. **internal-lb-udp** - This template creates a UDP Internal LB with a single Backend Pool, one Load Balancing Rule, FrontEnd and BackEnd ports set to 80 and HealthProbe URL can be set to a custom URL. The backend VMs can be added by developer teams using the resource ID of the Load Balancer BackendPool.
`Parameters:
Protocol - UDP,
Backend Pool - One,
LB Rule - One,
FrontEnd Port - Any UDP Port,
BackEend Port - Any UDP Port,
Health Probe - No Custom URL`
