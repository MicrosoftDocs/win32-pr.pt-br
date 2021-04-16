---
description: Representa os dados de configuração do recurso de descarregamento de porta.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Classe Msvm_EthernetSwitchPortOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 150a7b5e54e371c11741dd7c763b0ae145354b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757414"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a><span data-ttu-id="c7b48-103">\_Classe Msvm EthernetSwitchPortOffloadSettingData</span><span class="sxs-lookup"><span data-stu-id="c7b48-103">Msvm\_EthernetSwitchPortOffloadSettingData class</span></span>

<span data-ttu-id="c7b48-104">Representa os dados de configuração do recurso de descarregamento de porta.</span><span class="sxs-lookup"><span data-stu-id="c7b48-104">Represents the port offload feature setting data.</span></span>

<span data-ttu-id="c7b48-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c7b48-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b48-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7b48-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a><span data-ttu-id="c7b48-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c7b48-107">Members</span></span>

<span data-ttu-id="c7b48-108">A classe **Msvm \_ EthernetSwitchPortOffloadSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7b48-108">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c7b48-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7b48-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7b48-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7b48-110">Properties</span></span>

<span data-ttu-id="c7b48-111">A classe **Msvm \_ EthernetSwitchPortOffloadSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c7b48-111">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7b48-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c7b48-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7b48-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7b48-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7b48-115">A short description of the object.</span></span> <span data-ttu-id="c7b48-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de descarga de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="c7b48-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="c7b48-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c7b48-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7b48-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7b48-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="c7b48-120">A description of the object.</span></span> <span data-ttu-id="c7b48-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa os dados de configuração do recurso de descarregamento de porta.".</span><span class="sxs-lookup"><span data-stu-id="c7b48-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="c7b48-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c7b48-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7b48-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7b48-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c7b48-125">A display name for the object.</span></span> <span data-ttu-id="c7b48-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de descarga de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="c7b48-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="c7b48-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c7b48-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7b48-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7b48-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-130">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c7b48-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-131">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c7b48-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c7b48-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c7b48-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7b48-133">**IOVInterruptModeration**</span><span class="sxs-lookup"><span data-stu-id="c7b48-133">**IOVInterruptModeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-136">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-136">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-137">O valor de moderação de interrupção para descarregamento de IOV (virtualização de e/s).</span><span class="sxs-lookup"><span data-stu-id="c7b48-137">The interrupt moderation value for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="c7b48-138">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c7b48-138">The default is 0.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="c7b48-139">**Padrão** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-139">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

<span data-ttu-id="c7b48-140">**Adaptável** (1)</span><span class="sxs-lookup"><span data-stu-id="c7b48-140">**Adaptive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="c7b48-141">**Desativado** (2)</span><span class="sxs-lookup"><span data-stu-id="c7b48-141">**Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="c7b48-142">**Baixo** (100)</span><span class="sxs-lookup"><span data-stu-id="c7b48-142">**Low** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="c7b48-143">**Médio** (200)</span><span class="sxs-lookup"><span data-stu-id="c7b48-143">**Medium** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="c7b48-144">**Alta** (300)</span><span class="sxs-lookup"><span data-stu-id="c7b48-144">**High** (300)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7b48-145">**IOVOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="c7b48-145">**IOVOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-148">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-148">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-149">O peso atribuído a essa porta para descarregamento de IOV (virtualização de e/s).</span><span class="sxs-lookup"><span data-stu-id="c7b48-149">The weight assigned to this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="c7b48-150">O peso é a importância relativa ao atribuir recursos de IOV.</span><span class="sxs-lookup"><span data-stu-id="c7b48-150">The weight is the relative importance when assigning IOV resources.</span></span> <span data-ttu-id="c7b48-151">A definição da propriedade **IOVOffloadWeight** como 0 desabilita o descarregamento de IOV na porta.</span><span class="sxs-lookup"><span data-stu-id="c7b48-151">Setting the **IOVOffloadWeight** property to 0 disables IOV offloading on the port.</span></span> <span data-ttu-id="c7b48-152">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c7b48-152">The default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="c7b48-153">**IOVQueuePairsRequested**</span><span class="sxs-lookup"><span data-stu-id="c7b48-153">**IOVQueuePairsRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-154">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-156">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-156">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-157">O número de pares de fila solicitados para esta porta para o descarregamento de IOV (virtualização de e/s).</span><span class="sxs-lookup"><span data-stu-id="c7b48-157">The number of queue pairs requested for this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="c7b48-158">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="c7b48-158">The default is 1.</span></span>

</dd> <dt>

<span data-ttu-id="c7b48-159">**IPSecOffloadLimit**</span><span class="sxs-lookup"><span data-stu-id="c7b48-159">**IPSecOffloadLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-161">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-162">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-162">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-163">O número máximo de Slots de descarga de associação de segurança (SA) permitidos da porta.</span><span class="sxs-lookup"><span data-stu-id="c7b48-163">The maximum number of security association (SA) offload slots allowed from the port.</span></span>

</dd> <dt>

<span data-ttu-id="c7b48-164">**PacketDirectModerationCount**</span><span class="sxs-lookup"><span data-stu-id="c7b48-164">**PacketDirectModerationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-167">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-167">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-168">O valor da contagem de moderação de interrupção para o pacote (PD) direto. O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c7b48-168">The interrupt moderation count value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-169">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c7b48-169">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-170">**PacketDirectModerationInterval**</span><span class="sxs-lookup"><span data-stu-id="c7b48-170">**PacketDirectModerationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-173">Qualificadores: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-173">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-174">O valor do intervalo de moderação de interrupção para o pacote (PD) direto. O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c7b48-174">The interrupt moderation interval value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-175">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c7b48-175">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-176">**PacketDirectNumProcs**</span><span class="sxs-lookup"><span data-stu-id="c7b48-176">**PacketDirectNumProcs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-178">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-179">Qualificadores: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-179">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-180">O número de processadores usados pelo host para processar pacotes enviados desta porta no modo de pacote direto.</span><span class="sxs-lookup"><span data-stu-id="c7b48-180">The number of processors used by the host for processing packets sent from this port in Packet Direct mode.</span></span> <span data-ttu-id="c7b48-181">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="c7b48-181">The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-182">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c7b48-182">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-183">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="c7b48-183">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7b48-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-185">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-186">Qualificadores: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-186">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-187">Habilite o descarregamento de VMMQ se houver suporte do hardware. O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="c7b48-187">Enable VMMQ offload if supported by hardware.The default is False.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-188">Essa propriedade foi adicionada no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c7b48-188">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-189">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="c7b48-189">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-190">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-191">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-192">Qualificadores: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-192">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-193">O número de filas a serem alocadas quando o VRSS estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="c7b48-193">The number of queues to allocate when VRSS is enabled.</span></span> <span data-ttu-id="c7b48-194">O padrão é 16.</span><span class="sxs-lookup"><span data-stu-id="c7b48-194">The default is 16.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-195">Essa propriedade foi adicionada no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c7b48-195">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-196">**VMQOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="c7b48-196">**VMQOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-198">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-199">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-200">O peso atribuído a essa porta para o descarregamento da VMQ (fila de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="c7b48-200">The weight assigned to this port for virtual machine queue (VMQ) offloading.</span></span> <span data-ttu-id="c7b48-201">O peso é a importância relativa ao atribuir recursos de VMQ.</span><span class="sxs-lookup"><span data-stu-id="c7b48-201">The weight is the relative importance when assigning VMQ resources.</span></span> <span data-ttu-id="c7b48-202">Definir a propriedade **VMQOffloadWeight** como 0 DESABILITA a VMQ na porta.</span><span class="sxs-lookup"><span data-stu-id="c7b48-202">Setting the **VMQOffloadWeight** property to 0 disables VMQ on the port.</span></span> <span data-ttu-id="c7b48-203">O padrão é 100.</span><span class="sxs-lookup"><span data-stu-id="c7b48-203">The default is 100.</span></span>

</dd> <dt>

<span data-ttu-id="c7b48-204">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="c7b48-204">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-205">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7b48-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-206">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-207">Qualificadores: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-207">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-208">Habilitar VRSS.</span><span class="sxs-lookup"><span data-stu-id="c7b48-208">Enable VRSS.</span></span> <span data-ttu-id="c7b48-209">O padrão é true.</span><span class="sxs-lookup"><span data-stu-id="c7b48-209">The default is true.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-210">Essa propriedade foi adicionada no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c7b48-210">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-211">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="c7b48-211">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-212">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7b48-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-213">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-213">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-214">Qualificadores: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-214">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-215">Se o processador de VMQ primário deve ser excluído da tabela de indireção VRSS quando o VRSS está habilitado. O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="c7b48-215">Whether to exclude primary VMQ processor from the VRSS indirection table when VRSS is enabled.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-216">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="c7b48-216">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-217">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="c7b48-217">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-218">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7b48-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-219">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-219">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-220">Qualificadores: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-220">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-221">Se deseja sempre fazer o VRSS do lado do host quando o VRSS estiver habilitado, independentemente da configuração de RSS da NIC virtual. O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="c7b48-221">Whether to always do host-side VRSS when VRSS is enabled, regardless of RSS setting of the virtual NIC.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-222">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="c7b48-222">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-223">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="c7b48-223">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-224">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-225">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-225">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-226">Qualificadores: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-226">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-227">O número mínimo de filas a serem alocadas quando o VRSS estiver habilitado. O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="c7b48-227">The minimum number of queues to allocate when VRSS is enabled.The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-228">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="c7b48-228">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-229">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="c7b48-229">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-230">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-231">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-231">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-232">Qualificadores: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-232">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-233">O modo de agendamento de fila a ser usado quando o VRSS estiver habilitado. O padrão é o agendamento estático.</span><span class="sxs-lookup"><span data-stu-id="c7b48-233">The queue scheduling mode to use when VRSS is enabled.The default is static scheduling.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-234">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="c7b48-234">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="c7b48-235">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="c7b48-235">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b48-236">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b48-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-237">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c7b48-237">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c7b48-238">Qualificadores: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b48-238">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c7b48-239">A política de afinidade de canal VMBus a ser usada quando o VRSS estiver habilitado. O padrão é Strong.</span><span class="sxs-lookup"><span data-stu-id="c7b48-239">The vmbus channel affinity policy to use when VRSS is enabled.The default is strong.</span></span>

> [!Note]  
> <span data-ttu-id="c7b48-240">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="c7b48-240">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7b48-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7b48-241">Requirements</span></span>



| <span data-ttu-id="c7b48-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7b48-242">Requirement</span></span> | <span data-ttu-id="c7b48-243">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b48-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b48-244">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7b48-244">Minimum supported client</span></span><br/> | <span data-ttu-id="c7b48-245">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c7b48-245">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7b48-246">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7b48-246">Minimum supported server</span></span><br/> | <span data-ttu-id="c7b48-247">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c7b48-247">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7b48-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7b48-248">Namespace</span></span><br/>                | <span data-ttu-id="c7b48-249">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c7b48-249">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7b48-250">MOF</span><span class="sxs-lookup"><span data-stu-id="c7b48-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7b48-251"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7b48-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7b48-252">DLL</span><span class="sxs-lookup"><span data-stu-id="c7b48-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7b48-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7b48-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

