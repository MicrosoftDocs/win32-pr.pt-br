---
description: Uma associação usada para estabelecer relações entre uma instância de um Msvm \_ EmulatedEthernetPortSettingData e uma ou mais instâncias de um Msvm \_ EthernetSwitchFeatureSettingData.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Classe Msvm_EthernetPortFailoverSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50fff8688beea91495014dd75b1f1c33020869f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505929"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a><span data-ttu-id="15190-103">\_Classe Msvm EthernetPortFailoverSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="15190-103">Msvm\_EthernetPortFailoverSettingDataComponent class</span></span>

<span data-ttu-id="15190-104">Uma associação usada para estabelecer relações entre uma instância de um [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) e uma ou mais instâncias de um [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="15190-104">An association used to establish relationships between one instance of an [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="15190-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="15190-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15190-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15190-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="15190-107">Membros</span><span class="sxs-lookup"><span data-stu-id="15190-107">Members</span></span>

<span data-ttu-id="15190-108">A classe **Msvm \_ EthernetPortFailoverSettingDataComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="15190-108">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="15190-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="15190-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15190-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="15190-110">Properties</span></span>

<span data-ttu-id="15190-111">A classe **Msvm \_ EthernetPortFailoverSettingDataComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="15190-111">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15190-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="15190-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15190-113">Tipo de dados: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="15190-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="15190-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15190-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15190-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15190-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15190-116">Uma referência a uma instância da classe [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) ou [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) que representa a porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="15190-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="15190-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="15190-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15190-118">Tipo de dados: **[ **Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="15190-118">Data type: **[**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="15190-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15190-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15190-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="15190-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="15190-121">Uma referência a uma instância da classe [**Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) que representa a configuração do adaptador de rede convidado.</span><span class="sxs-lookup"><span data-stu-id="15190-121">A reference to an instance of the [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) class that represents the guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15190-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15190-122">Requirements</span></span>



| <span data-ttu-id="15190-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="15190-123">Requirement</span></span> | <span data-ttu-id="15190-124">Valor</span><span class="sxs-lookup"><span data-stu-id="15190-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15190-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15190-125">Minimum supported client</span></span><br/> | <span data-ttu-id="15190-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="15190-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="15190-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15190-127">Minimum supported server</span></span><br/> | <span data-ttu-id="15190-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="15190-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15190-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="15190-129">Namespace</span></span><br/>                | <span data-ttu-id="15190-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="15190-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="15190-131">MOF</span><span class="sxs-lookup"><span data-stu-id="15190-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15190-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15190-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15190-133">DLL</span><span class="sxs-lookup"><span data-stu-id="15190-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15190-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15190-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

