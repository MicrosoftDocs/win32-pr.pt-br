---
description: Representa as configurações de descarregamento de comutador.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Classe Msvm_EthernetSwitchHardwareOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760853"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a><span data-ttu-id="960a2-103">\_Classe Msvm EthernetSwitchHardwareOffloadSettingData</span><span class="sxs-lookup"><span data-stu-id="960a2-103">Msvm\_EthernetSwitchHardwareOffloadSettingData class</span></span>

<span data-ttu-id="960a2-104">Representa as configurações de descarregamento de comutador.</span><span class="sxs-lookup"><span data-stu-id="960a2-104">Represents the switch offload settings.</span></span>

<span data-ttu-id="960a2-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="960a2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="960a2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="960a2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a><span data-ttu-id="960a2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="960a2-107">Members</span></span>

<span data-ttu-id="960a2-108">A classe **Msvm \_ EthernetSwitchHardwareOffloadSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="960a2-108">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="960a2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="960a2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="960a2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="960a2-110">Properties</span></span>

<span data-ttu-id="960a2-111">A classe **Msvm \_ EthernetSwitchHardwareOffloadSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="960a2-111">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="960a2-112">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="960a2-112">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960a2-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="960a2-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="960a2-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="960a2-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="960a2-115">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="960a2-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="960a2-116">Especifica as configurações de VMMQ para a fila padrão do vSwitch.</span><span class="sxs-lookup"><span data-stu-id="960a2-116">Specifies the VMMQ settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="960a2-117">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="960a2-117">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960a2-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="960a2-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="960a2-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="960a2-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="960a2-120">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="960a2-120">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="960a2-121">Especifica o número de filas para a fila padrão.</span><span class="sxs-lookup"><span data-stu-id="960a2-121">Specifies the number of queues for the default queue.</span></span>

</dd> <dt>

<span data-ttu-id="960a2-122">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="960a2-122">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960a2-123">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="960a2-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="960a2-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="960a2-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="960a2-125">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="960a2-125">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="960a2-126">Especifica as configurações de VRss para a fila padrão do vSwitch.</span><span class="sxs-lookup"><span data-stu-id="960a2-126">Specifies the VRss settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="960a2-127">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="960a2-127">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960a2-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="960a2-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="960a2-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="960a2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="960a2-130">Qualificadores: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="960a2-130">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="960a2-131">Indica se a CPU de VMQ primária foi excluída da tabela de indireção VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="960a2-131">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="960a2-132">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="960a2-132">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="960a2-133">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="960a2-133">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960a2-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="960a2-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="960a2-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="960a2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="960a2-136">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="960a2-136">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="960a2-137">Indica se a difusão do VRSS deve ser sempre feita para a fila padrão, independentemente do estado de RSS do vPort externo.</span><span class="sxs-lookup"><span data-stu-id="960a2-137">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="960a2-138">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="960a2-138">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="960a2-139">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="960a2-139">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960a2-140">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="960a2-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="960a2-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="960a2-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="960a2-142">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="960a2-142">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="960a2-143">Indica o número mínimo de filas usadas para VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="960a2-143">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="960a2-144">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="960a2-144">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="960a2-145">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="960a2-145">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960a2-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="960a2-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="960a2-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="960a2-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="960a2-148">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="960a2-148">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="960a2-149">Indica como as filas VRSS/VMMQ são direcionadas para processadores de host diferentes.</span><span class="sxs-lookup"><span data-stu-id="960a2-149">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="960a2-150">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="960a2-150">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="960a2-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="960a2-151">Requirements</span></span>



| <span data-ttu-id="960a2-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="960a2-152">Requirement</span></span> | <span data-ttu-id="960a2-153">Valor</span><span class="sxs-lookup"><span data-stu-id="960a2-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="960a2-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="960a2-154">Minimum supported client</span></span><br/> | <span data-ttu-id="960a2-155">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="960a2-155">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="960a2-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="960a2-156">Minimum supported server</span></span><br/> | <span data-ttu-id="960a2-157">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="960a2-157">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="960a2-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="960a2-158">Namespace</span></span><br/>                | <span data-ttu-id="960a2-159">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="960a2-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="960a2-160">MOF</span><span class="sxs-lookup"><span data-stu-id="960a2-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="960a2-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="960a2-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="960a2-162">DLL</span><span class="sxs-lookup"><span data-stu-id="960a2-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="960a2-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="960a2-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="960a2-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="960a2-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960a2-165">**Msvm \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="960a2-165">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




