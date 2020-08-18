# AZ 301 Study => Mission Accomplished :)

Exam Link: https://docs.microsoft.com/en-us/learn/certifications/exams/az-301

Topics: https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE3VEHD (Guide by topics)

### Topics
- [x] Determine Workload Requirements (10 - 15%)
- [x] Design for Identity and security (20 - 25%) -- AD is very important for AZ301
- [x] Design a Data Platform Solution (15 - 20%)
- [x] Design a Business Continuity Strategy (15 - 20%)
- [x] Design for Deployment, Migration and Integration (10 - 15%)
- [x] Design an Infrastructure Strategy (15 - 20%)

# Quick Overview Study
- [x] https://learn.acloud.guru/course/az-301-architect-design/dashboard -- done, great course to polish your knowhow !!!
- [ ] https://www.skylinesacademy.com/resources -- study guides, section az 301 -- links to related azure documentation
- [ ] https://www.linkedin.com/learning/exam-tips-microsoft-azure-architect-design-az-301 -- exam tips
- [ ] https://docs.microsoft.com/en-us/azure/architecture/ -- azure architecture center
- [x] [Microsoft Azure Architect Technologies - Exam AZ-300, James Lee](https://linuxacademy.com/cp/modules/view/id/280?redirect_uri=https://app.linuxacademy.com/search?categories=Azure&type=Course&difficulty=Advanced) -- done mostly
- [x] [Microsoft Azure Arcitect Design - Exam AZ-301, James Lee](https://linuxacademy.com/cp/modules/view/id/381?redirect_uri=https://app.linuxacademy.com/search?query=az%20301) -- done mostly, great course!
- [ ] https://www.udemy.com/course/az301-azure/learn/lecture/16028996#overview
- [ ] https://interactive.linuxacademy.com/diagrams/TheBlueShiftGuide.html
- [x] https://interactive.linuxacademy.com/diagrams/AzureArchitectDesign.html

### Microsoft Learn (works in IE)

# More Resources
- [ ] https://app.pluralsight.com/paths/certificate/microsoft-azure-architect-technologies-az-300
- [ ] https://app.pluralsight.com/paths/certificate/microsoft-azure-architect-design-az-301
- [ ] [Exam Prep | AZ-301: Microsoft Azure Architect Design](https://www.youtube.com/watch?v=q0zKXHWRmgo)
- [ ] https://www.udemy.com/course/70534-azure/learn/lecture/17313412#overview
- [ ] https://www.udemy.com/course/az-300-azure-architecture-technologies-practice-test/learn/quiz/4584274/test#overview
- [ ] https://github.com/MicrosoftLearning/AZ-301-MicrosoftAzureArchitectDesign
- [ ] [ Microsoft Azure Architect Technologies - Exam AZ-300  - LinuxAcademy](https://linuxacademy.com/cp/modules/view/id/280)
- [ ] https://www.linkedin.com/learning/paths/prepare-for-microsoft-azure-architect-technologies-certification-az-300
- [ ] https://www.linkedin.com/learning/exam-tips-microsoft-azure-architect-design-az-301
- [ ] General: https://docs.microsoft.com/en-us/learn/browse/?products=azure&roles=solution-architect&source=learn


# Notes
- List existing vnets: az network vnet list --output table
- Create subnet: az network vnet subnet create -g vnet1rg --vnet-name vnet1 -n subnet2 --address-prefix 10.1.2.0/24
- Create a NIC: az network nic create -g vnet1rg --vnet-name vnet1 --subnet subnet1 -n nic1
- Get NIC info: $nic1 = Get-AzureRmNetworkInterface -ResourceGroupName vnet1rg -Name nic1
- Get public IP info: $pubip = Get-AzureRmPublicIpAddress -ResourceGroupName lab01rg -name pubip01
- Get NIC IP Config: $nic1.ipconfigurations, $nic1.ipconfigurations[0]
- Get public IP of NIC IP configuration 0: $nic1.ipconfigurations[0].PublicIPAddress
- Assign public IP: $nic1.ipconfigurations[0].PublicIPAddress = $pubip
- Set updated configuration: Set-AzureRmNetworkInterface -NetworkInterface $nic1
- Get image publishers: Get-AzureRmVmImagePublisher -location australiasoutheast | select publishername
- Get image offer: Get-AzureRmVmImageOffer -Location australiasoutheast -publisher canonical | Select Offer
- Get image SKU: Get-AzureRmVmImageSku -Location australiasoutheast -Publisher canonical -Offer UbuntuServer | Select Skus
- Get image: Get-AzureRMVMImage -Location australiasoutheast -Publisher canonical -Offer ubuntuserver -Sku 16.04-lts | Select Version
- Set VM source image: Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 16.04-LTS -version latest
- Create storage account: New-AzureRmStorageAccount -ResourceGroupName lab01rg -AccountName lalabsa02 -Location australiaeast -Kind BlobStorage -SkuName Standard_GRS -AccessTier Hot
- Create storage account: New-AzureRmStorageAccount -ResourceGroupName lab01rg -AccountName lalabsa03 -Location australiaeast -Kind Storage -SkuName Standard_LRS
- Configure service endpoint: az network vnet subnet update -g vnet1rg --vnet-name vnet1 -n subnet1 --service-endpoints "Microsoft.Storage"
- Log queries:
  * AzureActivity | limit 50
  * AzureActivity | where OperationName == "Regenerate Storage Account Keys"
  * AzureActivity | where Caller == "adm.jlee@laaz.onmicrosoft.com"
- Create VNet peer: az network vnet peering create -g vnet1rg -n vnet1-to-vnet3-peer --vnet-name vnet1 --remote-vnet /subscriptions/xx-xx-xx/resourceGroups/vnet3rg/providers/Microsoft.Network/virtualNetworks/vnet3 --allow-vnet-access
- Create return VNet peer: az network vnet peering create -g vnet3rg -n vnet3-to-vnet1-peer --vnet-name vnet3 --remote-vnet /subscriptions/xx-xx-xx/resourceGroups/vnet1rg/providers/Microsoft.Network/virtualNetworks/vnet1 --allow-vnet-access
- New resource group: New-AzureRmResourceGroup -name deploytestrg -Location "Australia Southeast"
- Secure password: $pw = Read-Host "Enter Pass" -AsSecureString
- New deployment: New-AzureRmResourceGroupDeployment -ResourceGroupName deploytestrg -TemplateUri uri -adminUsername adm-jlee -adminPassword $pw
- To create a custom role from our JSON definition: az role definition create --role-definition ./customRole.json
- We could also assign the role from CLI: az role assignment create --role LAAzureAdmin --assignee username --resource-group rgname
- Failing to use a routable-domain for the user-principal name (UPN) can result in login issues
- Syncrhonization Service Manager allows management of the connectors and synchronization profiles
- Synchronization can be triggered using: Start-ADSyncSyncCycle:
  * PolicyType Intial option is for the initial sync
  * PolicyType Delta is for differential sync
- In staging mode, synchronization will run (both automatically or if you use the command) but will not do an actual export to Azure AD
- Save our vnet1 information to a variable: $vnet1 = Get-AzureRmVirtualNetwork -ResourceGroupName vnet1rg -Name vnet1
- Save our GatewaySubnet information to a variable: $gwsubnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "GatewaySubnet" -VirtualNetwork $vnet1
- Create a public IP for the VNet gateway: $gwIP = New-AzureRmPublicIpAddress -name "ergwip01" -ResourceGroupName $vnet1.ResourceGroupName -Location $vnet1.Location -AllocationMethod Dynamic
- Create the VNet gateway network config: $gwconfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name "ergw01IpConfig" -SubnetId $gwsubnet.Id -PublicIpAddressId $gwIP.Id
- Create the VNet gateway: $gw = New-AzureRmVirtualNetworkGateway -Name "ergw01" -ResourceGroupName $vnet1.ResourceGroupName -Location $vnet1.Location -IpConfigurations $gwconfig -GatewayType "ExpressRoute" -GatewaySku Standard
- To build our image: docker build -t hellola-web:v1 .
- To create the registry: az acr create --resource-group containersrg --name laazreg01 --sku Basic
- To prepare our image: docker tag hellola-web:v1 laazreg01.azurecr.io/hellola-web:v1
- To log into our registry: docker login laazreg01.azurecr.io
- To upload our image: Docker push laazreg01.azurecr.io/hellola-web:v1
- Retrieve the token: curl 'http://169.254.169.254/metadata/identity/oauth2/token?api-version=2018-02-01&resource=https://management.azure.com/' -H Metadata:true
- Retrieving resource group info: curl -H "Authorization: Bearer <TOKEN>" https://management.azure.com/subscriptions/<SUB>/resourceGroups/<RG>?api-version=2016-09-01
- Retrieve resource group info: curl -H "Authorization: Bearer <TOKEN>" https://management.azure.com/subscriptions/<SUB>/resourceGroups/1?api-version=2016-09-01
- Delete resource group: curl -X DELETE https://management.azure.com/subscriptions/<SUB>/resourceGroups/<RG>?api-version=2018-05-01 -H "Authorization: Bearer <TOKEN>
- Enabling encryption: az vm encryption enable -g vmencrypt -n vmencrypt --disk-encryption-keyvault /subscriptions/c95fdfe4-2593-410e-8901-3de366c89013/resourceGroups/keyvault01org/providers/Microsoft.KeyVault/vaults/laazkv01
- Showing the VM encryption status: az vm encryption show -g vmencrypt -n vmencrypt

