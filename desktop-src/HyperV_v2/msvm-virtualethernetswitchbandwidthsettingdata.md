---
description: Representa as configurações de largura de banda de um comutador virtual.
ms.assetid: bc6f8cd3-f74a-4f4a-9ffe-a88def3966d9
title: Classe Msvm_VirtualEthernetSwitchBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchBandwidthSettingData
- Msvm_VirtualEthernetSwitchBandwidthSettingData.InstanceID
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Caption
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Description
- Msvm_VirtualEthernetSwitchBandwidthSettingData.ElementName
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowReservation
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec94409366761ee208d3e8a6af59a4d07527d82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752471"
---
# <a name="msvm_virtualethernetswitchbandwidthsettingdata-class"></a><span data-ttu-id="1e2d5-103">\_Classe Msvm VirtualEthernetSwitchBandwidthSettingData</span><span class="sxs-lookup"><span data-stu-id="1e2d5-103">Msvm\_VirtualEthernetSwitchBandwidthSettingData class</span></span>

<span data-ttu-id="1e2d5-104">Representa as configurações de largura de banda de um comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="1e2d5-104">Represents the bandwidth settings for a virtual switch.</span></span>

<span data-ttu-id="1e2d5-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1e2d5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2d5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e2d5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("3EB2B8E8-4ABF-4DBF-9071-16DD47481FBE"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchBandwidthSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  string InstanceID = "Microsoft:Definition\GUID\Default";
  string Caption = "Ethernet Switch Bandwidth Settings";
  string Description = "Represents the switch bandwidth settings.";
  string ElementName = "Ethernet Switch Bandwidth Settings";
  UINT64 DefaultFlowReservation = 0;
  UINT64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="1e2d5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1e2d5-107">Members</span></span>

<span data-ttu-id="1e2d5-108">A classe **Msvm \_ VirtualEthernetSwitchBandwidthSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1e2d5-108">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1e2d5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e2d5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e2d5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e2d5-110">Properties</span></span>

<span data-ttu-id="1e2d5-111">A classe **Msvm \_ VirtualEthernetSwitchBandwidthSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1e2d5-111">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e2d5-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2d5-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e2d5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e2d5-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1e2d5-115">A short description of the object.</span></span> <span data-ttu-id="1e2d5-116">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e é sempre definida como "configurações de largura de banda do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="1e2d5-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="1e2d5-117">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-117">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2d5-118">Tipo de dados: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-118">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1e2d5-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-120">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1e2d5-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1e2d5-121">Especifica a reserva de largura de banda absoluta para fluxos não classificados no adaptador subjacente.</span><span class="sxs-lookup"><span data-stu-id="1e2d5-121">Specifies the absolute bandwidth reservation for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e2d5-122">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-122">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2d5-123">Tipo de dados: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-123">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1e2d5-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-125">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="1e2d5-125">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1e2d5-126">Especifica a reserva de largura de banda em peso para fluxos não classificados no adaptador subjacente.</span><span class="sxs-lookup"><span data-stu-id="1e2d5-126">Specifies the bandwidth reservation in weight for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1e2d5-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2d5-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e2d5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e2d5-130">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="1e2d5-130">A description of the object.</span></span> <span data-ttu-id="1e2d5-131">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa as configurações de largura de banda do comutador.".</span><span class="sxs-lookup"><span data-stu-id="1e2d5-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the switch bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="1e2d5-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2d5-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e2d5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e2d5-135">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1e2d5-135">A display name for the object.</span></span> <span data-ttu-id="1e2d5-136">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como "configurações de largura de banda do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="1e2d5-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="1e2d5-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2d5-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e2d5-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e2d5-140">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1e2d5-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1e2d5-141">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="1e2d5-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1e2d5-142">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) e é sempre definida como "Microsoft: \\ *GUID* de definição \\ padrão".</span><span class="sxs-lookup"><span data-stu-id="1e2d5-142">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:Definition\\*GUID*\\Default".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e2d5-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e2d5-143">Requirements</span></span>



| <span data-ttu-id="1e2d5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e2d5-144">Requirement</span></span> | <span data-ttu-id="1e2d5-145">Valor</span><span class="sxs-lookup"><span data-stu-id="1e2d5-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2d5-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e2d5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2d5-147">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1e2d5-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1e2d5-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e2d5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2d5-149">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1e2d5-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e2d5-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e2d5-150">Namespace</span></span><br/>                | <span data-ttu-id="1e2d5-151">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1e2d5-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1e2d5-152">MOF</span><span class="sxs-lookup"><span data-stu-id="1e2d5-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e2d5-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e2d5-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e2d5-154">DLL</span><span class="sxs-lookup"><span data-stu-id="1e2d5-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e2d5-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e2d5-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

