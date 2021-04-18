---
description: Representa as configurações de largura de banda da porta.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Classe Msvm_EthernetSwitchPortBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760852"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a><span data-ttu-id="e69b2-103">\_Classe Msvm EthernetSwitchPortBandwidthSettingData</span><span class="sxs-lookup"><span data-stu-id="e69b2-103">Msvm\_EthernetSwitchPortBandwidthSettingData class</span></span>

<span data-ttu-id="e69b2-104">Representa as configurações de largura de banda da porta.</span><span class="sxs-lookup"><span data-stu-id="e69b2-104">Represents the port bandwidth settings.</span></span>

<span data-ttu-id="e69b2-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e69b2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e69b2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e69b2-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a><span data-ttu-id="e69b2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e69b2-107">Members</span></span>

<span data-ttu-id="e69b2-108">A classe **Msvm \_ EthernetSwitchPortBandwidthSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e69b2-108">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e69b2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e69b2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e69b2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e69b2-110">Properties</span></span>

<span data-ttu-id="e69b2-111">A classe **Msvm \_ EthernetSwitchPortBandwidthSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e69b2-111">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e69b2-112">**BurstLimit**</span><span class="sxs-lookup"><span data-stu-id="e69b2-112">**BurstLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-113">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e69b2-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e69b2-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-115">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e69b2-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-116">A largura de banda de pico permitida da porta durante intermitências.</span><span class="sxs-lookup"><span data-stu-id="e69b2-116">The peak bandwidth allowed from the port during bursts.</span></span>

</dd> <dt>

<span data-ttu-id="e69b2-117">**BurstSize**</span><span class="sxs-lookup"><span data-stu-id="e69b2-117">**BurstSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-118">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e69b2-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e69b2-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-120">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e69b2-120">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-121">O tamanho máximo de intermitência permitido.</span><span class="sxs-lookup"><span data-stu-id="e69b2-121">The maximum burst size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="e69b2-122">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e69b2-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e69b2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e69b2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-125">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e69b2-125">A short description of the object.</span></span> <span data-ttu-id="e69b2-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de largura de banda da porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="e69b2-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="e69b2-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e69b2-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e69b2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e69b2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-130">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="e69b2-130">A description of the object.</span></span> <span data-ttu-id="e69b2-131">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa as configurações de largura de banda da porta".</span><span class="sxs-lookup"><span data-stu-id="e69b2-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="e69b2-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e69b2-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e69b2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e69b2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-135">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e69b2-135">A display name for the object.</span></span> <span data-ttu-id="e69b2-136">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de largura de banda da porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="e69b2-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="e69b2-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e69b2-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e69b2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e69b2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-140">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e69b2-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-141">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="e69b2-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e69b2-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e69b2-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e69b2-143">**Limite**</span><span class="sxs-lookup"><span data-stu-id="e69b2-143">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-144">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e69b2-144">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e69b2-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-146">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e69b2-146">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-147">O limite de largura de banda permitido para a porta.</span><span class="sxs-lookup"><span data-stu-id="e69b2-147">The bandwidth limit allowed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="e69b2-148">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="e69b2-148">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-149">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e69b2-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e69b2-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-151">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e69b2-151">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-152">A largura de banda absoluta mínima garantida para a porta.</span><span class="sxs-lookup"><span data-stu-id="e69b2-152">The minimum absolute bandwidth guaranteed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="e69b2-153">**Weight**</span><span class="sxs-lookup"><span data-stu-id="e69b2-153">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b2-154">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e69b2-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e69b2-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e69b2-156">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e69b2-156">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e69b2-157">A largura de banda mínima em peso garantida para a porta.</span><span class="sxs-lookup"><span data-stu-id="e69b2-157">The minimum bandwidth in weight guaranteed for the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e69b2-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e69b2-158">Requirements</span></span>



| <span data-ttu-id="e69b2-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="e69b2-159">Requirement</span></span> | <span data-ttu-id="e69b2-160">Valor</span><span class="sxs-lookup"><span data-stu-id="e69b2-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69b2-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e69b2-161">Minimum supported client</span></span><br/> | <span data-ttu-id="e69b2-162">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e69b2-162">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e69b2-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e69b2-163">Minimum supported server</span></span><br/> | <span data-ttu-id="e69b2-164">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e69b2-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e69b2-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="e69b2-165">Namespace</span></span><br/>                | <span data-ttu-id="e69b2-166">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e69b2-166">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e69b2-167">MOF</span><span class="sxs-lookup"><span data-stu-id="e69b2-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e69b2-168"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e69b2-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e69b2-169">DLL</span><span class="sxs-lookup"><span data-stu-id="e69b2-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e69b2-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e69b2-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

