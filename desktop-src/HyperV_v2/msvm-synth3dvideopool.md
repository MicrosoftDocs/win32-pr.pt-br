---
description: Contém informações sobre as GPUs (unidades de processamento de gráficos de vídeo) 3D sintéticas disponíveis no sistema host.
ms.assetid: 771A42C3-4888-49DF-A389-161A2D0E3DBD
title: Classe Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool
- Msvm_Synth3dVideoPool.InstanceID
- Msvm_Synth3dVideoPool.Caption
- Msvm_Synth3dVideoPool.Description
- Msvm_Synth3dVideoPool.ElementName
- Msvm_Synth3dVideoPool.InstallDate
- Msvm_Synth3dVideoPool.Name
- Msvm_Synth3dVideoPool.OperationalStatus
- Msvm_Synth3dVideoPool.StatusDescriptions
- Msvm_Synth3dVideoPool.Status
- Msvm_Synth3dVideoPool.HealthState
- Msvm_Synth3dVideoPool.CommunicationStatus
- Msvm_Synth3dVideoPool.DetailedStatus
- Msvm_Synth3dVideoPool.OperatingStatus
- Msvm_Synth3dVideoPool.PrimaryStatus
- Msvm_Synth3dVideoPool.PoolID
- Msvm_Synth3dVideoPool.Primordial
- Msvm_Synth3dVideoPool.Capacity
- Msvm_Synth3dVideoPool.Reserved
- Msvm_Synth3dVideoPool.ResourceType
- Msvm_Synth3dVideoPool.OtherResourceType
- Msvm_Synth3dVideoPool.ResourceSubType
- Msvm_Synth3dVideoPool.AllocationUnits
- Msvm_Synth3dVideoPool.ConsumedResourceUnits
- Msvm_Synth3dVideoPool.CurrentlyConsumedResource
- Msvm_Synth3dVideoPool.MaxConsumableResource
- Msvm_Synth3dVideoPool.Is3dVideoSupported
- Msvm_Synth3dVideoPool.IsSLATCapable
- Msvm_Synth3dVideoPool.IsGPUCapable
- Msvm_Synth3dVideoPool.DirectXVersion
- Msvm_Synth3dVideoPool.RequiredMinimumDirectXVersion
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1afad0f1b2e80a747bb518cb3eafc75d494de62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921380"
---
# <a name="msvm_synth3dvideopool-class"></a><span data-ttu-id="afc13-103">\_Classe Msvm Synth3dVideoPool</span><span class="sxs-lookup"><span data-stu-id="afc13-103">Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="afc13-104">Contém informações sobre as GPUs (unidades de processamento de gráficos de vídeo) 3D sintéticas disponíveis no sistema host.</span><span class="sxs-lookup"><span data-stu-id="afc13-104">Contains information about the synthetic 3-D video graphics processing units (GPUs) available on the host system.</span></span> <span data-ttu-id="afc13-105">Essa classe é usada somente com sistemas host que dão suporte a RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="afc13-105">This class is only used with host systems that support RemoteFX.</span></span>

<span data-ttu-id="afc13-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="afc13-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc13-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afc13-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synth3dVideoPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption = "3D Display Controller Resource Pool";
  string   Description = "Resource pool used to allocate synthetic 3D video controller resources to a virtual machine.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID;
  boolean  Primordial = True;
  uint64   Capacity;
  uint64   Reserved = 0;
  uint16   ResourceType;
  string   OtherResourceType;
  string   ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string   AllocationUnits = "count";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
  boolean  Is3dVideoSupported;
  boolean  IsSLATCapable;
  boolean  IsGPUCapable;
  string   DirectXVersion;
  string   RequiredMinimumDirectXVersion;
};
```

## <a name="members"></a><span data-ttu-id="afc13-108">Membros</span><span class="sxs-lookup"><span data-stu-id="afc13-108">Members</span></span>

<span data-ttu-id="afc13-109">A classe **Msvm \_ Synth3dVideoPool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="afc13-109">The **Msvm\_Synth3dVideoPool** class has these types of members:</span></span>

-   [<span data-ttu-id="afc13-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="afc13-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="afc13-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afc13-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="afc13-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="afc13-112">Methods</span></span>

<span data-ttu-id="afc13-113">A classe **Msvm \_ Synth3dVideoPool** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="afc13-113">The **Msvm\_Synth3dVideoPool** class has these methods.</span></span>



| <span data-ttu-id="afc13-114">Método</span><span class="sxs-lookup"><span data-stu-id="afc13-114">Method</span></span>                                                                                             | <span data-ttu-id="afc13-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="afc13-115">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afc13-116">**CalculateVideoMemoryRequirements**</span><span class="sxs-lookup"><span data-stu-id="afc13-116">**CalculateVideoMemoryRequirements**</span></span>](msvm-synth3dvideopool-calculatevideomemoryrequirements.md) | <span data-ttu-id="afc13-117">Calcula a quantidade de memória de vídeo necessária para uma máquina virtual do RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="afc13-117">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="afc13-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afc13-118">Properties</span></span>

<span data-ttu-id="afc13-119">A classe **Msvm \_ Synth3dVideoPool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="afc13-119">The **Msvm\_Synth3dVideoPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afc13-120">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="afc13-120">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-123">As unidades de alocação usadas pelo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="afc13-123">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="afc13-124">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="afc13-124">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-125">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="afc13-125">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afc13-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-128">A quantidade máxima (em unidades de **AllocationUnits**) de reservas ativas às quais o pool de recursos pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="afc13-128">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="afc13-129">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="afc13-129">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-130">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="afc13-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afc13-133">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="afc13-133">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="afc13-134">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="afc13-134">A short description of the object.</span></span> <span data-ttu-id="afc13-135">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="afc13-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-137">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afc13-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-139">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="afc13-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="afc13-140">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="afc13-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="afc13-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="afc13-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="afc13-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="afc13-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="afc13-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="afc13-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="afc13-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="afc13-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="afc13-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="afc13-149">)</span><span class="sxs-lookup"><span data-stu-id="afc13-149">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="afc13-150">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="afc13-150">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-153">Especifica as unidades para as propriedades **MaxConsumableResource** e **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="afc13-153">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="afc13-154">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="afc13-154">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-155">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="afc13-155">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-156">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afc13-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-158">Especifica a quantidade de recursos que o pool de recursos apresenta atualmente aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="afc13-158">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="afc13-159">Essa propriedade é diferente da propriedade **reservada** , pois descreve a exibição de consumidores do recurso, enquanto a propriedade **reservada** descreve a exibição de produtores do recurso.</span><span class="sxs-lookup"><span data-stu-id="afc13-159">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="afc13-160">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="afc13-160">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-161">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="afc13-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-164">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="afc13-164">A description of the object.</span></span> <span data-ttu-id="afc13-165">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="afc13-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afc13-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-169">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="afc13-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="afc13-170">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="afc13-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="afc13-171">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="afc13-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="afc13-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="afc13-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="afc13-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="afc13-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="afc13-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="afc13-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="afc13-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="afc13-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="afc13-180">)</span><span class="sxs-lookup"><span data-stu-id="afc13-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="afc13-181">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="afc13-181">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afc13-184">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="afc13-184">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="afc13-185">Especifica a versão mais baixa do DirectX que é suportada pelos cartões dentro do pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="afc13-185">Specifies the lowest version of DirectX that is supported by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="afc13-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="afc13-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-189">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="afc13-189">A display name for the object.</span></span> <span data-ttu-id="afc13-190">Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="afc13-190">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="afc13-191">A propriedade [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) da classe **CIM \_ ManagedSystemElement** também é definida como um nome de exibição, mas geralmente ela é subclasseda para ser uma chave.</span><span class="sxs-lookup"><span data-stu-id="afc13-191">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name, but it is often subclassed to be a Key.</span></span> <span data-ttu-id="afc13-192">Não é razoável que a mesma propriedade possa transmitir a identidade e um nome de exibição, sem inconsistências.</span><span class="sxs-lookup"><span data-stu-id="afc13-192">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="afc13-193">Onde [**Name**](msvm-keyboard.md) existe e não é uma chave (como para instâncias de LogicalDevice), as mesmas informações podem estar presentes nas propriedades **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="afc13-193">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="afc13-194">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="afc13-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afc13-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-198">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="afc13-198">The current health of the element.</span></span> <span data-ttu-id="afc13-199">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="afc13-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="afc13-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-201">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="afc13-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-203">A data e a hora em que a máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="afc13-203">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="afc13-204">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-205">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="afc13-205">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afc13-208">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="afc13-208">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="afc13-209">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="afc13-209">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="afc13-210">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-211">**Is3dVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="afc13-211">**Is3dVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-212">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="afc13-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-214">Especifica se há suporte para o vídeo 3D no sistema host.</span><span class="sxs-lookup"><span data-stu-id="afc13-214">Specifies whether 3-D video is supported by the host system.</span></span> <span data-ttu-id="afc13-215">Contém um valor diferente de zero se o vídeo 3D tiver suporte ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="afc13-215">Contains a nonzero value if 3-D video is supported, or zero otherwise.</span></span> <span data-ttu-id="afc13-216">Para oferecer suporte a vídeo 3D, o host do RemoteFX deve ter recursos de conversão de endereços de segundo nível (SLAT) e ter pelo menos uma GPU física que dê suporte a RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="afc13-216">To support 3-D video, the RemoteFX host must have second level address translation (SLAT) capabilities and have at least one physical GPU that supports RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="afc13-217">**IsGPUCapable**</span><span class="sxs-lookup"><span data-stu-id="afc13-217">**IsGPUCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-218">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="afc13-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-220">Especifica se o host tem GPUs que dão suporte a RemoteFX e se suas versões do DirectX atendem ao requisito mínimo.</span><span class="sxs-lookup"><span data-stu-id="afc13-220">Specifies whether the host has GPUs that support RemoteFX and whether their DirectX versions meet the minimum requirement.</span></span>

</dd> <dt>

<span data-ttu-id="afc13-221">**IsSLATCapable**</span><span class="sxs-lookup"><span data-stu-id="afc13-221">**IsSLATCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-222">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="afc13-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afc13-224">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")</span><span class="sxs-lookup"><span data-stu-id="afc13-224">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="afc13-225">Especifica se o host tem uma CPU compatível com SLAT (conversão de endereços de segundo nível).</span><span class="sxs-lookup"><span data-stu-id="afc13-225">Specifies whether the host has a second level address translation (SLAT) capable CPU.</span></span>

> [!Note]  
> <span data-ttu-id="afc13-226">Preterido no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="afc13-226">Deprecated in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="afc13-227">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="afc13-227">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-228">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afc13-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-230">Especifica a quantidade máxima de recursos consumíveis que o pool de recursos pode apresentar aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="afc13-230">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="afc13-231">Essa propriedade é diferente da propriedade **Capacity** , pois descreve a exibição de consumidores do recurso, enquanto a propriedade **Capacity** descreve a exibição de produtores do recurso.</span><span class="sxs-lookup"><span data-stu-id="afc13-231">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="afc13-232">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="afc13-232">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-233">**Nome**</span><span class="sxs-lookup"><span data-stu-id="afc13-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afc13-236">Qualificadores: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="afc13-236">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="afc13-237">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="afc13-237">The label by which the object is known.</span></span> <span data-ttu-id="afc13-238">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="afc13-238">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="afc13-239">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-240">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="afc13-240">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-241">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afc13-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-243">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="afc13-243">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="afc13-244">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="afc13-244">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="afc13-245">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="afc13-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="afc13-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="afc13-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="afc13-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="afc13-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="afc13-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="afc13-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="afc13-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="afc13-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="afc13-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="afc13-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="afc13-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="afc13-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="afc13-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="afc13-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="afc13-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="afc13-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="afc13-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="afc13-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="afc13-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="afc13-265">)</span><span class="sxs-lookup"><span data-stu-id="afc13-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="afc13-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="afc13-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-267">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afc13-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="afc13-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-269">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="afc13-269">The current status of the element.</span></span> <span data-ttu-id="afc13-270">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="afc13-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span> <span data-ttu-id="afc13-271">O Hyper-V nunca usará apenas o primeiro elemento dessa matriz.</span><span class="sxs-lookup"><span data-stu-id="afc13-271">Hyper-V will only ever use the first element of this array.</span></span>

</dd> <dt>

<span data-ttu-id="afc13-272">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="afc13-272">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-275">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorpool.md) é definido como 0 ("other").</span><span class="sxs-lookup"><span data-stu-id="afc13-275">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="afc13-276">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="afc13-276">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="afc13-277">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="afc13-277">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-280">Esse valor é referenciado pelas instâncias do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que foram alocadas deste pool.</span><span class="sxs-lookup"><span data-stu-id="afc13-280">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="afc13-281">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é sempre definida como "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="afc13-281">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="afc13-282">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="afc13-282">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-283">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afc13-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-285">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="afc13-285">Provides high level status information.</span></span> <span data-ttu-id="afc13-286">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="afc13-286">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="afc13-287">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="afc13-287">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="afc13-288">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="afc13-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="afc13-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="afc13-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="afc13-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="afc13-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="afc13-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="afc13-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="afc13-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="afc13-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="afc13-295">)</span><span class="sxs-lookup"><span data-stu-id="afc13-295">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="afc13-296">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="afc13-296">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-297">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="afc13-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-299">**True** se esse pool de recursos for a base da qual os recursos são desenhados e retornados na atividade do gerenciamento de recursos; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="afc13-299">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="afc13-300">Ser primordial significa que esse pool de recursos não pode ser criado ou excluído por consumidores desse modelo.</span><span class="sxs-lookup"><span data-stu-id="afc13-300">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="afc13-301">No entanto, outras ações, modeladas ou não, podem afetar as características ou o tamanho dos pools de recursos primordial.</span><span class="sxs-lookup"><span data-stu-id="afc13-301">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="afc13-302">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="afc13-302">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-303">**RequiredMinimumDirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="afc13-303">**RequiredMinimumDirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afc13-306">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="afc13-306">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="afc13-307">Especifica a versão mais baixa do DirectX que é exigida pelos cartões dentro do pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="afc13-307">Specifies the lowest version of DirectX that is required by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="afc13-308">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="afc13-308">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-309">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afc13-309">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-311">As reservas atuais (em unidades de **AllocationUnits**) se espalham por todas as alocações ativas deste pool.</span><span class="sxs-lookup"><span data-stu-id="afc13-311">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="afc13-312">Em uma configuração hierárquica, isso representa a soma de todas as reservas atuais do pool de recursos descendentes.</span><span class="sxs-lookup"><span data-stu-id="afc13-312">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="afc13-313">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="afc13-313">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-314">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="afc13-314">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-317">Uma cadeia de caracteres que descreve um subtipo específico de implementação para este pool.</span><span class="sxs-lookup"><span data-stu-id="afc13-317">A string that describes an implementation specific subtype for this pool.</span></span> <span data-ttu-id="afc13-318">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="afc13-318">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="afc13-319">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="afc13-319">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="afc13-320">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="afc13-320">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-321">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afc13-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-323">O tipo de recurso que esse pool de recursos pode alocar.</span><span class="sxs-lookup"><span data-stu-id="afc13-323">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="afc13-324">Essa propriedade é herdada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))e é sempre definida como 4 ("memória").</span><span class="sxs-lookup"><span data-stu-id="afc13-324">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="afc13-325">**Status**</span><span class="sxs-lookup"><span data-stu-id="afc13-325">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afc13-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-328">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="afc13-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="afc13-329">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="afc13-329">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afc13-330">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afc13-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="afc13-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afc13-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afc13-332">Cadeias de caracteres que descrevem os vários valores de matriz de [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="afc13-332">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="afc13-333">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="afc13-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span> <span data-ttu-id="afc13-334">O Hyper-V nunca usará apenas o primeiro elemento dessa matriz.</span><span class="sxs-lookup"><span data-stu-id="afc13-334">Hyper-V will only ever use the first element of this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afc13-335">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afc13-335">Requirements</span></span>



| <span data-ttu-id="afc13-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc13-336">Requirement</span></span> | <span data-ttu-id="afc13-337">Valor</span><span class="sxs-lookup"><span data-stu-id="afc13-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc13-338">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afc13-338">Minimum supported client</span></span><br/> | <span data-ttu-id="afc13-339">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="afc13-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="afc13-340">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afc13-340">Minimum supported server</span></span><br/> | <span data-ttu-id="afc13-341">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="afc13-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="afc13-342">Namespace</span><span class="sxs-lookup"><span data-stu-id="afc13-342">Namespace</span></span><br/>                | <span data-ttu-id="afc13-343">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="afc13-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="afc13-344">MOF</span><span class="sxs-lookup"><span data-stu-id="afc13-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afc13-345"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afc13-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="afc13-346">DLL</span><span class="sxs-lookup"><span data-stu-id="afc13-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afc13-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="afc13-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="afc13-348">Confira também</span><span class="sxs-lookup"><span data-stu-id="afc13-348">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc13-349">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="afc13-349">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> </dl>

 

