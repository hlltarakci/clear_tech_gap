# AZ 301 Study

Exam Link: https://docs.microsoft.com/en-us/learn/certifications/exams/az-301

Topics: https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE3VEHD (Guide by topics)

# Quick Overview Study
- [ ] [Microsoft Azure Architect Technologies - Exam AZ-300, James Lee](https://linuxacademy.com/cp/modules/view/id/280?redirect_uri=https://app.linuxacademy.com/search?categories=Azure&type=Course&difficulty=Advanced) -- in progress
- [ ] https://www.udemy.com/course/az-300-azure-architecture-technologies-practice-test/learn/quiz/4584274/test#overview
- [ ] https://www.udemy.com/course/az301-azure/learn/lecture/16028996#overview

# More Resources
- [ ] https://app.pluralsight.com/paths/certificate/microsoft-azure-architect-technologies-az-300
- [ ] https://app.pluralsight.com/paths/certificate/microsoft-azure-architect-design-az-301
- [ ] [Exam Prep | AZ-301: Microsoft Azure Architect Design](https://www.youtube.com/watch?v=q0zKXHWRmgo)
- [ ] https://interactive.linuxacademy.com/diagrams/TheBlueShiftGuide.html
- [ ] https://interactive.linuxacademy.com/diagrams/AzureArchitectDesign.html
- [ ] https://www.udemy.com/course/70534-azure/learn/lecture/17313412#overview
- [ ] https://github.com/MicrosoftLearning/AZ-301-MicrosoftAzureArchitectDesign
- [ ] [ Microsoft Azure Architect Technologies - Exam AZ-300  - LinuxAcademy](https://linuxacademy.com/cp/modules/view/id/280)
- [ ] https://www.linkedin.com/learning/paths/prepare-for-microsoft-azure-architect-technologies-certification-az-300
- [ ] https://www.linkedin.com/learning/exam-tips-microsoft-azure-architect-design-az-301


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
