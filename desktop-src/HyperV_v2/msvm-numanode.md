---
description: Representa um nó NUMA (acesso não uniforme à memória) de um sistema virtual.
ms.assetid: a2e9aa74-15e5-4a78-b7f8-ffe2883a31d0
title: Classe Msvm_NumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NumaNode
- Msvm_NumaNode.RequestStateChange
- Msvm_NumaNode.InstanceID
- Msvm_NumaNode.Caption
- Msvm_NumaNode.Description
- Msvm_NumaNode.ElementName
- Msvm_NumaNode.InstallDate
- Msvm_NumaNode.Name
- Msvm_NumaNode.OperationalStatus
- Msvm_NumaNode.StatusDescriptions
- Msvm_NumaNode.Status
- Msvm_NumaNode.HealthState
- Msvm_NumaNode.CommunicationStatus
- Msvm_NumaNode.DetailedStatus
- Msvm_NumaNode.OperatingStatus
- Msvm_NumaNode.PrimaryStatus
- Msvm_NumaNode.EnabledState
- Msvm_NumaNode.OtherEnabledState
- Msvm_NumaNode.RequestedState
- Msvm_NumaNode.EnabledDefault
- Msvm_NumaNode.TimeOfLastStateChange
- Msvm_NumaNode.AvailableRequestedStates
- Msvm_NumaNode.TransitioningToState
- Msvm_NumaNode.SystemCreationClassName
- Msvm_NumaNode.SystemName
- Msvm_NumaNode.CreationClassName
- Msvm_NumaNode.NodeID
- Msvm_NumaNode.NumberOfProcessorCores
- Msvm_NumaNode.NumberOfLogicalProcessors
- Msvm_NumaNode.CurrentlyConsumableMemoryBlocks
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4bdbd600cd4a78f66376f21ee264b2dfe9854147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783290"
---
# <a name="msvm_numanode-class"></a><span data-ttu-id="0dcbe-103">\_Classe Msvm NumaNode</span><span class="sxs-lookup"><span data-stu-id="0dcbe-103">Msvm\_NumaNode class</span></span>

<span data-ttu-id="0dcbe-104">Representa um nó NUMA (acesso não uniforme à memória) de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-104">Represents a Non-Uniform Memory Access (NUMA) node of a virtual system.</span></span>

<span data-ttu-id="0dcbe-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dcbe-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0dcbe-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_NumaNode : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NodeID;
  uint32   NumberOfProcessorCores;
  uint32   NumberOfLogicalProcessors;
  uint64   CurrentlyConsumableMemoryBlocks;
};
```

## <a name="members"></a><span data-ttu-id="0dcbe-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0dcbe-107">Members</span></span>

<span data-ttu-id="0dcbe-108">A classe **Msvm \_ NumaNode** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0dcbe-108">The **Msvm\_NumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="0dcbe-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0dcbe-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0dcbe-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0dcbe-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0dcbe-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="0dcbe-111">Methods</span></span>

<span data-ttu-id="0dcbe-112">A classe **Msvm \_ NumaNode** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-112">The **Msvm\_NumaNode** class has these methods.</span></span>



| <span data-ttu-id="0dcbe-113">Método</span><span class="sxs-lookup"><span data-stu-id="0dcbe-113">Method</span></span>                 | <span data-ttu-id="0dcbe-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dcbe-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="0dcbe-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-115">**RequestStateChange**</span></span> | <span data-ttu-id="0dcbe-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-116">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0dcbe-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0dcbe-117">Properties</span></span>

<span data-ttu-id="0dcbe-118">A classe **Msvm \_ NumaNode** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-118">The **Msvm\_NumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0dcbe-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-120">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-122">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="0dcbe-122">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="0dcbe-123">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-123">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-127">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-127">A short description of the object.</span></span> <span data-ttu-id="0dcbe-128">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-132">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0dcbe-133">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0dcbe-134">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0dcbe-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0dcbe-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0dcbe-142">)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0dcbe-143">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-143">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-146">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-147">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-147">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-148">**CurrentlyConsumableMemoryBlocks**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-148">**CurrentlyConsumableMemoryBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-149">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-151">O número de blocos de memória disponíveis no momento para consumo por máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-151">The number of memory blocks currently available for consumption by virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-152">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-155">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="0dcbe-155">A description of the object.</span></span> <span data-ttu-id="0dcbe-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-158">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-160">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0dcbe-161">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0dcbe-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0dcbe-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0dcbe-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0dcbe-171">)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0dcbe-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-175">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-175">A display name for the object.</span></span> <span data-ttu-id="0dcbe-176">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-177">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-177">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-178">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-180">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-180">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0dcbe-181">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-181">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-182">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-182">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-183">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-185">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-185">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0dcbe-186">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-186">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0dcbe-187">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="0dcbe-188">Valor</span><span class="sxs-lookup"><span data-stu-id="0dcbe-188">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="0dcbe-189">Significado</span><span class="sxs-lookup"><span data-stu-id="0dcbe-189">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="0dcbe-190"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="0dcbe-190"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="0dcbe-191">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-191">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="0dcbe-192"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-192"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="0dcbe-193"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-193"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="0dcbe-194">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-194">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="0dcbe-195"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-195"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="0dcbe-196">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-196">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="0dcbe-197"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-197"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="0dcbe-198">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-198">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="0dcbe-199"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="0dcbe-200">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-200">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="0dcbe-201"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="0dcbe-202">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-202">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="0dcbe-203"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-203"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="0dcbe-204">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-204">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="0dcbe-205"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-205"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="0dcbe-206">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-206">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="0dcbe-207"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-207"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="0dcbe-208">O elemento está habilitado, mas está em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-208">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="0dcbe-209">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-209">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="0dcbe-210">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-210">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="0dcbe-211"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-211"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="0dcbe-212">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-212">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="0dcbe-213">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-213">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="0dcbe-214">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-214">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-215">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-217">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-217">The current health of the element.</span></span> <span data-ttu-id="0dcbe-218">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-218">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0dcbe-219">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-219">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0dcbe-220">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-221">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-221">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-222">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-222">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-224">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-224">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0dcbe-225">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-226">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-226">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-229">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-229">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-230">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-230">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0dcbe-231">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-232">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-232">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-235">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-235">The label by which the object is known.</span></span> <span data-ttu-id="0dcbe-236">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-237">**NodeID**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-237">**NodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-238">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-240">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-240">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-241">O identificador de nó NUMA.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-241">The NUMA node identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-242">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-242">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-243">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-245">O número total de núcleos lógicos do processador neste nó.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-245">The total number of logical processor cores in this node.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-246">**NumberOfProcessorCores**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-246">**NumberOfProcessorCores**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-247">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-249">O número total de núcleos de processador neste nó NUMA.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-249">The total number of processor cores in this NUMA node.</span></span> <span data-ttu-id="0dcbe-250">Isso pode ser diferente do número de objetos do [**\_ processador Msvm**](msvm-processor.md) associados a esse nó se cada núcleo do processador der suporte a vários threads de computação.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-250">This may differ from the number of [**Msvm\_Processor**](msvm-processor.md) objects associated to this node if each processor core supports multiple compute threads.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-251">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-251">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-252">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-254">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="0dcbe-254">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0dcbe-255">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0dcbe-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0dcbe-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0dcbe-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0dcbe-276">)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-276">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0dcbe-277">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-277">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-278">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-278">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-280">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-280">The current statuses of the object.</span></span> <span data-ttu-id="0dcbe-281">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-282">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-282">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-283">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-285">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-285">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0dcbe-286">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-286">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0dcbe-287">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-288">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-288">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-289">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-291">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-291">Provides high level status information.</span></span> <span data-ttu-id="0dcbe-292">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-292">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0dcbe-293">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0dcbe-294">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0dcbe-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0dcbe-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0dcbe-301">)</span><span class="sxs-lookup"><span data-stu-id="0dcbe-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0dcbe-302">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-302">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-303">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-305">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-305">The last requested or desired state for the element.</span></span> <span data-ttu-id="0dcbe-306">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-306">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0dcbe-307">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-307">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0dcbe-308">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="0dcbe-308">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="0dcbe-309">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-309">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="0dcbe-310">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-310">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-311">**Status**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-311">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-315">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-315">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-316">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-316">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-318">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0dcbe-318">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0dcbe-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-320">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-320">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-323">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="0dcbe-323">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-324">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-324">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-325">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-325">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-328">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="0dcbe-328">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-329">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-329">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-330">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-330">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-331">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-333">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-333">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0dcbe-334">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como "NULL".</span><span class="sxs-lookup"><span data-stu-id="0dcbe-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="0dcbe-335">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-335">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dcbe-336">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0dcbe-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0dcbe-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0dcbe-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0dcbe-338">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="0dcbe-338">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0dcbe-339">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0dcbe-339">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0dcbe-340">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dcbe-340">Requirements</span></span>



| <span data-ttu-id="0dcbe-341">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dcbe-341">Requirement</span></span> | <span data-ttu-id="0dcbe-342">Valor</span><span class="sxs-lookup"><span data-stu-id="0dcbe-342">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dcbe-343">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dcbe-343">Minimum supported client</span></span><br/> | <span data-ttu-id="0dcbe-344">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0dcbe-344">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0dcbe-345">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dcbe-345">Minimum supported server</span></span><br/> | <span data-ttu-id="0dcbe-346">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0dcbe-346">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0dcbe-347">Namespace</span><span class="sxs-lookup"><span data-stu-id="0dcbe-347">Namespace</span></span><br/>                | <span data-ttu-id="0dcbe-348">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0dcbe-348">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0dcbe-349">MOF</span><span class="sxs-lookup"><span data-stu-id="0dcbe-349">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0dcbe-350"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-350"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0dcbe-351">DLL</span><span class="sxs-lookup"><span data-stu-id="0dcbe-351">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dcbe-352"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0dcbe-352"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

