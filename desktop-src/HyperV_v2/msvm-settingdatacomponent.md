---
description: Estabeleça uma relação entre uma instância da classe Msvm \_ EmulatedEthernetPortSettingData ou Msvm \_ SyntheticEthernetPortSettingData com uma instância da \_ classe Msvm GuestNetworkAdapterConfiguration.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Classe Msvm_SettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922051"
---
# <a name="msvm_settingdatacomponent-class"></a><span data-ttu-id="c6d01-103">\_Classe Msvm SettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="c6d01-103">Msvm\_SettingDataComponent class</span></span>

<span data-ttu-id="c6d01-104">Estabeleça uma relação entre uma instância da classe [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) ou [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) com uma instância da classe Msvm [**\_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="c6d01-104">Establish a relationship between an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class with an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span>

<span data-ttu-id="c6d01-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c6d01-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d01-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6d01-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c6d01-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c6d01-107">Members</span></span>

<span data-ttu-id="c6d01-108">A classe **Msvm \_ SettingDataComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c6d01-108">The **Msvm\_SettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="c6d01-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6d01-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6d01-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6d01-110">Properties</span></span>

<span data-ttu-id="c6d01-111">A classe **Msvm \_ SettingDataComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c6d01-111">The **Msvm\_SettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6d01-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c6d01-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d01-113">Tipo de dados: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="c6d01-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="c6d01-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c6d01-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d01-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c6d01-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c6d01-116">Uma referência a uma instância da classe [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) ou [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) que representa uma porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c6d01-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="c6d01-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c6d01-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d01-118">Tipo de dados: **[ **Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span><span class="sxs-lookup"><span data-stu-id="c6d01-118">Data type: **[**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c6d01-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c6d01-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d01-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="c6d01-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c6d01-121">Uma referência a uma instância da classe [**Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) que representa uma configuração de adaptador de rede de convidado.</span><span class="sxs-lookup"><span data-stu-id="c6d01-121">A reference to an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class that represents a guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6d01-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6d01-122">Requirements</span></span>



| <span data-ttu-id="c6d01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6d01-123">Requirement</span></span> | <span data-ttu-id="c6d01-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c6d01-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d01-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6d01-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d01-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c6d01-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c6d01-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6d01-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d01-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c6d01-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6d01-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6d01-129">Namespace</span></span><br/>                | <span data-ttu-id="c6d01-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c6d01-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c6d01-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c6d01-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6d01-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6d01-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6d01-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c6d01-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6d01-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c6d01-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

