---
description: Descreve dados de configurações para um comutador Ethernet virtual.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: Classe CIM_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769346"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="2772b-103">\_Classe CIM VirtualEthernetSwitchSettingData</span><span class="sxs-lookup"><span data-stu-id="2772b-103">CIM\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="2772b-104">Descreve dados de configurações para um comutador Ethernet virtual.</span><span class="sxs-lookup"><span data-stu-id="2772b-104">Describes settings data for a virtual ethernet switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="2772b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2772b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="2772b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2772b-106">Members</span></span>

<span data-ttu-id="2772b-107">A classe **CIM \_ VirtualEthernetSwitchSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2772b-107">The **CIM\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2772b-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2772b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2772b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2772b-109">Properties</span></span>

<span data-ttu-id="2772b-110">A classe **CIM \_ VirtualEthernetSwitchSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2772b-110">The **CIM\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2772b-111">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="2772b-111">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2772b-112">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2772b-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2772b-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2772b-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2772b-114">Uma matriz que contém os pools de recursos de host que estão associados atualmente ou para associar ao comutador Ethernet, a fim de alocar conexões Ethernet entre o comutador Ethernet e uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2772b-114">An array that contains the host resource pools that are currently associated, or to associate with the ethernet switch, in order to allocate ethernet connections between the ethernet switch and a virtual machine.</span></span> <span data-ttu-id="2772b-115">Cada valor não nulo dessa propriedade deve estar de acordo com **o \_ \_ UntypedInstancePath do URI WBEM** , conforme definido na especificação "DSP0207" de DMTF.</span><span class="sxs-lookup"><span data-stu-id="2772b-115">Each non-Null value of this property must conform to **WBEM\_URI\_UntypedInstancePath** as defined in the DMTF "DSP0207" specification.</span></span>

</dd> <dt>

<span data-ttu-id="2772b-116">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="2772b-116">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2772b-117">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2772b-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2772b-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2772b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2772b-119">O número de endereços MAC exclusivos que o comutador pode aprender para o aprendizado de endereço MAC, conforme definido no padrão IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="2772b-119">The number of unique MAC addresses that the switch can learn for MAC address learning, as defined in the IEEE 802.1 standard.</span></span>

</dd> <dt>

<span data-ttu-id="2772b-120">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="2772b-120">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2772b-121">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2772b-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2772b-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2772b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2772b-123">Uma matriz que contém as IDs de VLAN que o comutador pode acessar.</span><span class="sxs-lookup"><span data-stu-id="2772b-123">An array that contains the VLAN IDs that the switch can access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2772b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2772b-124">Requirements</span></span>



| <span data-ttu-id="2772b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2772b-125">Requirement</span></span> | <span data-ttu-id="2772b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2772b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2772b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2772b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2772b-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2772b-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2772b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2772b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2772b-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2772b-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2772b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="2772b-131">Namespace</span></span><br/>                | <span data-ttu-id="2772b-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2772b-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2772b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2772b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2772b-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2772b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2772b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2772b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2772b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2772b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2772b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2772b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2772b-138">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="2772b-138">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




