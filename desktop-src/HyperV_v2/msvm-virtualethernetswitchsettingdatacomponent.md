---
description: Uma associação usada para estabelecer &\# 0034; parte de&\# 0034; relações entre uma instância de Msvm \_ VirtualEthernetSwitchSettingData e uma ou mais instâncias de Msvm \_ EthernetSwitchFeatureSettingData.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Classe Msvm_VirtualEthernetSwitchSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165245"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a><span data-ttu-id="2d84a-103">\_Classe Msvm VirtualEthernetSwitchSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="2d84a-103">Msvm\_VirtualEthernetSwitchSettingDataComponent class</span></span>

<span data-ttu-id="2d84a-104">Uma associação usada para estabelecer relações "parte de" entre uma instância de [**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) e uma ou mais instâncias do [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="2d84a-104">An association used to establish "part of" relationships between one instance of [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) and one or more instances of [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="2d84a-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2d84a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d84a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d84a-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2d84a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2d84a-107">Members</span></span>

<span data-ttu-id="2d84a-108">A classe **Msvm \_ VirtualEthernetSwitchSettingDataComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2d84a-108">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2d84a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2d84a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d84a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2d84a-110">Properties</span></span>

<span data-ttu-id="2d84a-111">A classe **Msvm \_ VirtualEthernetSwitchSettingDataComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2d84a-111">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d84a-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2d84a-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d84a-113">Tipo de dados: **Msvm \_ VirtualEthernetSwitchSettingData**</span><span class="sxs-lookup"><span data-stu-id="2d84a-113">Data type: **Msvm\_VirtualEthernetSwitchSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2d84a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2d84a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d84a-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2d84a-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2d84a-116">Referência a uma instância da classe [**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) que representa uma porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="2d84a-116">Reference to an instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="2d84a-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2d84a-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d84a-118">Tipo de dados: **Msvm \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="2d84a-118">Data type: **Msvm\_EthernetSwitchFeatureSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2d84a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2d84a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d84a-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="2d84a-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2d84a-121">Referência a uma instância da classe [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) que representa as configurações aplicadas à opção.</span><span class="sxs-lookup"><span data-stu-id="2d84a-121">Reference to an instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that represents the settings applied to the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d84a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d84a-122">Requirements</span></span>



| <span data-ttu-id="2d84a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d84a-123">Requirement</span></span> | <span data-ttu-id="2d84a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2d84a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d84a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d84a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d84a-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2d84a-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2d84a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d84a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d84a-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2d84a-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d84a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d84a-129">Namespace</span></span><br/>                | <span data-ttu-id="2d84a-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2d84a-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2d84a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2d84a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d84a-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d84a-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d84a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2d84a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d84a-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d84a-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

