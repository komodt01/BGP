
# Routing Security Checklist

- [ ] Use MD5 authentication for all BGP peers
- [ ] Apply prefix-lists and route maps
- [ ] Validate expected subnets only are received
- [ ] Monitor BGP session status (CloudWatch, Azure Monitor)
- [ ] Set route limits to prevent flooding
- [ ] Segment route tables (TGW, ExpressRoute Gateway)
- [ ] Enable flow logs in all clouds
