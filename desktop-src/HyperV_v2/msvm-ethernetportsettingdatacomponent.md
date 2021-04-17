---
description: Uma associação usada para estabelecer &\# 0034; parte de&\# 0034; relações entre uma instância de um \_ EthernetPortAllocationSettingData Msvm e uma ou mais instâncias de um \_ EthernetSwitchFeatureSettingData Msvm.
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Classe Msvm_EthernetPortSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755103"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a><span data-ttu-id="5f324-103">\_Classe Msvm EthernetPortSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="5f324-103">Msvm\_EthernetPortSettingDataComponent class</span></span>

<span data-ttu-id="5f324-104">Uma associação usada para estabelecer relações "parte de" entre uma instância de um [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) e uma ou mais instâncias de um [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="5f324-104">An association used to establish "part of" relationships between one instance of an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="5f324-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5f324-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f324-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f324-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="5f324-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5f324-107">Members</span></span>

<span data-ttu-id="5f324-108">A classe **Msvm \_ EthernetPortSettingDataComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f324-108">The **Msvm\_EthernetPortSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="5f324-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f324-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f324-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f324-110">Properties</span></span>

<span data-ttu-id="5f324-111">A classe **Msvm \_ EthernetPortSettingDataComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f324-111">The **Msvm\_EthernetPortSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f324-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5f324-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f324-113">Tipo de dados: **[ **Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="5f324-113">Data type: **[**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5f324-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f324-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f324-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f324-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f324-116">Uma referência a uma instância da classe [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que representa a porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5f324-116">A reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="5f324-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5f324-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f324-118">Tipo de dados: **[ **Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="5f324-118">Data type: **[**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5f324-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f324-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f324-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="5f324-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5f324-121">Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representa as configurações de recurso aplicadas à porta.</span><span class="sxs-lookup"><span data-stu-id="5f324-121">A reference to an instance of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the feature settings applied to the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f324-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f324-122">Requirements</span></span>



| <span data-ttu-id="5f324-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f324-123">Requirement</span></span> | <span data-ttu-id="5f324-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5f324-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f324-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f324-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5f324-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5f324-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5f324-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f324-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5f324-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5f324-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f324-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f324-129">Namespace</span></span><br/>                | <span data-ttu-id="5f324-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5f324-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5f324-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5f324-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f324-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f324-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f324-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5f324-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f324-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f324-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

