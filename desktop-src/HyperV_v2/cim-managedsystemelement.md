---
description: CIM \_ ManagedSystemElement é a classe base para a hierarquia de elementos do sistema. Qualquer componente de um sistema pode potencialmente ser representado por essa classe ou suas subclasses.
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: Classe CIM_ManagedSystemElement (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f16b84e24929d5cfdb6e5dd8855d69a8bce2dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170259"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a><span data-ttu-id="f2a6c-104">Classe CIM_ManagedSystemElement (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-104">CIM_ManagedSystemElement class (Hyper-V management)</span></span>

<span data-ttu-id="f2a6c-105">**CIM \_ ManagedSystemElement** é a classe base para a hierarquia de elementos do sistema.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-105">**CIM\_ManagedSystemElement** is the base class for the system element hierarchy.</span></span> <span data-ttu-id="f2a6c-106">Qualquer componente de um sistema pode potencialmente ser representado por essa classe ou suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-106">Any component of a system can potentially be represented by this class or its subclasses.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a6c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2a6c-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
};
```

## <a name="members"></a><span data-ttu-id="f2a6c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f2a6c-108">Members</span></span>

<span data-ttu-id="f2a6c-109">A classe **CIM \_ ManagedSystemElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f2a6c-109">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="f2a6c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2a6c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2a6c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2a6c-111">Properties</span></span>

<span data-ttu-id="f2a6c-112">A classe **CIM \_ ManagedSystemElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-112">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2a6c-113">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-113">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-116">Indica a capacidade da instrumentação de se comunicar com este elemento.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-116">Indicates the ability of the instrumentation to communicate with this element.</span></span> <span data-ttu-id="f2a6c-117">Um valor **nulo** indica que a instrumentação não oferece suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-117">A **NULL** value indicates that instrumentation does not support this property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2a6c-118">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="f2a6c-119">**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-119">**Not Available** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

<span data-ttu-id="f2a6c-120">**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-120">**Communication OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="f2a6c-121">**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-121">**Lost Communication** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f2a6c-122">**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-122">**No Contact** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f2a6c-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f2a6c-124">**Fornecedor reservado** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-124">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2a6c-125">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-125">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-128">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**","**CIM \_ ManagedSystemElement**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-129">Indica detalhes de status adicionais que complementam a propriedade **PrimaryStatus** .</span><span class="sxs-lookup"><span data-stu-id="f2a6c-129">Indicates additional status details that complement the **PrimaryStatus** property.</span></span> <span data-ttu-id="f2a6c-130">Um valor **nulo** indica que a instrumentação não oferece suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-130">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="f2a6c-131">**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-131">**Not Available** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

<span data-ttu-id="f2a6c-132">**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-132">**No Additional Information** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f2a6c-133">**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-133">**Stressed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="f2a6c-134">**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-134">**Predictive Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="f2a6c-135">**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-135">**Non-Recoverable Error** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="f2a6c-136">**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-136">**Supporting Entity in Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f2a6c-137">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f2a6c-138">**Fornecedor reservado** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-138">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2a6c-139">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-139">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-142">Indica a integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-142">Indicates the current health of the element.</span></span> <span data-ttu-id="f2a6c-143">Esse atributo expressa a integridade desse elemento, mas não necessariamente a integridade de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-143">This attribute expresses the health of this element, but not necessarily the health of its subcomponents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2a6c-144">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f2a6c-145">**OK** (5)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-145">**OK** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="f2a6c-146">**Degradado/aviso** (10)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-146">**Degraded/Warning** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

<span data-ttu-id="f2a6c-147">**Falha secundária** (15)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-147">**Minor failure** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

<span data-ttu-id="f2a6c-148">**Falha principal** (20)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-148">**Major failure** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

<span data-ttu-id="f2a6c-149">**Falha crítica** (25)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-149">**Critical failure** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="f2a6c-150">**Erro não recuperável** (30)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-150">**Non-recoverable error** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f2a6c-151">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-151">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2a6c-152">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-152">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-153">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-153">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-155">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-156">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-156">Indicates when the object was installed.</span></span> <span data-ttu-id="f2a6c-157">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-157">The lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="f2a6c-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-161">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-162">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-162">The label by which the object is known.</span></span> <span data-ttu-id="f2a6c-163">Quando em uma subclasse, a propriedade **Name** pode ser substituída como uma propriedade Key.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-163">When subclassed, the **Name** property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="f2a6c-164">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-164">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-167">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-168">Indica a condição operacional atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-168">Indicates the current operational condition of the element.</span></span> <span data-ttu-id="f2a6c-169">Essa propriedade pode ser usada para fornecer mais detalhes sobre o valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="f2a6c-169">This property can be used to provide more detail about the value of the **EnabledState** property.</span></span> <span data-ttu-id="f2a6c-170">Um valor **nulo** indica que a instrumentação não oferece suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-170">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<span data-ttu-id="f2a6c-171">"Unknown" indica</span><span class="sxs-lookup"><span data-stu-id="f2a6c-171">"Unknown" indicates</span></span>

<span data-ttu-id="f2a6c-172">"None" indica que</span><span class="sxs-lookup"><span data-stu-id="f2a6c-172">"None" indicates that</span></span>

<span data-ttu-id="f2a6c-173">Operações</span><span class="sxs-lookup"><span data-stu-id="f2a6c-173">"Servicing"</span></span>

<span data-ttu-id="f2a6c-174">Comece</span><span class="sxs-lookup"><span data-stu-id="f2a6c-174">"Starting"</span></span>

<span data-ttu-id="f2a6c-175">Impedir</span><span class="sxs-lookup"><span data-stu-id="f2a6c-175">"Stopping"</span></span>

<span data-ttu-id="f2a6c-176">"Parado" e "anulado" são semelhantes, embora o primeiro, enquanto o último i</span><span class="sxs-lookup"><span data-stu-id="f2a6c-176">"Stopped" and "Aborted" are similar, although the former , while the latter i</span></span>

<span data-ttu-id="f2a6c-177">"Inativo" indica que</span><span class="sxs-lookup"><span data-stu-id="f2a6c-177">"Dormant" indicates that</span></span>

<span data-ttu-id="f2a6c-178">"Concluído" indica que t</span><span class="sxs-lookup"><span data-stu-id="f2a6c-178">"Completed" indicates that t</span></span>

<span data-ttu-id="f2a6c-179">Migrando</span><span class="sxs-lookup"><span data-stu-id="f2a6c-179">"Migrating"</span></span>

<span data-ttu-id="f2a6c-180">"Immigrating"</span><span class="sxs-lookup"><span data-stu-id="f2a6c-180">"Immigrating"</span></span>

<span data-ttu-id="f2a6c-181">"Emigrating"</span><span class="sxs-lookup"><span data-stu-id="f2a6c-181">"Emigrating"</span></span>

<span data-ttu-id="f2a6c-182">"Desligando"</span><span class="sxs-lookup"><span data-stu-id="f2a6c-182">"Shutting Down"</span></span>

<span data-ttu-id="f2a6c-183">"Em teste"</span><span class="sxs-lookup"><span data-stu-id="f2a6c-183">"In Test"</span></span>

<span data-ttu-id="f2a6c-184">Transição</span><span class="sxs-lookup"><span data-stu-id="f2a6c-184">"Transitioning"</span></span>

<span data-ttu-id="f2a6c-185">"Em serviço"</span><span class="sxs-lookup"><span data-stu-id="f2a6c-185">"In Service"</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2a6c-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-187">A implementação é, em geral, capaz de retornar essa propriedade, mas não é possível fazer isso no momento.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-187">The implementation is in general capable of returning this property, but is unable to do so at this time.</span></span>

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="f2a6c-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-189">A implementação (provedor) é capaz de retornar um valor para essa propriedade, mas não para essa parte específica do hardware/software ou a propriedade não é usada intencionalmente porque não adiciona informações significativas (como no caso de uma propriedade que se destina a adicionar informações adicionais a outra propriedade).</span><span class="sxs-lookup"><span data-stu-id="f2a6c-189">The implementation (provider) is capable of returning a value for this property, but not ever for this particular piece of hardware/software or the property is intentionally not used because it adds no meaningful information (as in the case of a property that is intended to add additional info to another property).</span></span>

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span data-ttu-id="f2a6c-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-191">Descreve um elemento que está sendo configurado, mantido, limpo ou administrado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-191">Describes an element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f2a6c-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-193">Descreve um elemento que está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-193">Describes an element being initialized.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f2a6c-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-195">Descreve um elemento que está sendo trazido para uma parada ordenada.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-195">Describes an element being brought to an orderly stop.</span></span>

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="f2a6c-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-197">Ocorreu uma parada limpa e ordenada.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-197">A clean and orderly stop has occurred.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="f2a6c-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-199">Uma parada abrupta ocorreu, em que o estado e a configuração do elemento talvez precisem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-199">An abrupt stop has occurred, where the state and configuration of the element might need to be updated.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="f2a6c-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-201">O elemento está inativo ou desativado.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-201">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="f2a6c-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-203">O elemento concluiu sua operação.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-203">The element has completed its operation.</span></span> <span data-ttu-id="f2a6c-204">Esse valor deve ser combinado com OK, erro ou degradado no PrimaryStatus para que um cliente possa saber se a operação completa foi concluída com OK (aprovado), concluída com erro (com falha) ou concluída com degradado (a operação foi concluída, mas não foi concluída corretamente ou não relatou um erro).</span><span class="sxs-lookup"><span data-stu-id="f2a6c-204">This value should be combined with either OK, Error, or Degraded in the PrimaryStatus so that a client can tell if the complete operation Completed with OK (passed), Completed with Error (failed), or Completed with Degraded (the operation finished, but it did not complete OK or did not report an error).</span></span>

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span data-ttu-id="f2a6c-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-206">O elemento está sendo movido entre os elementos de host.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-206">The element is being moved between host elements.</span></span>

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span data-ttu-id="f2a6c-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-208">O elemento está sendo movido para fora do elemento de host.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-208">The element is being moved away from host element.</span></span>

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span data-ttu-id="f2a6c-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-210">O elemento está sendo movido para o novo elemento de host.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-210">The element is being moved to new host element.</span></span>

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span data-ttu-id="f2a6c-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="f2a6c-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-213">Descreve um elemento que está sendo trazido para uma parada abrupta.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-213">Describes an element being brought to an abrupt stop.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f2a6c-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-215">O elemento está executando funções de teste.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-215">The element is performing test functions.</span></span>

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span data-ttu-id="f2a6c-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-217">Descreve um elemento que está entre os Estados, ou seja, ele não está totalmente disponível em seu estado anterior ou em seu próximo estado.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-217">Describes an element that is between states, that is, it is not fully available in either its previous state or its next state.</span></span> <span data-ttu-id="f2a6c-218">Esse valor deve ser usado se outros valores que indicam uma transição para um estado específico não forem aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-218">This value should be used if other values indicating a transition to a specific state are not applicable.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="f2a6c-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-220">Descreve um elemento que está no serviço e operacional.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-220">Describes an element that is in service and operational.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f2a6c-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f2a6c-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2a6c-223">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-223">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-224">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-226">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM ManagedSystemElement**.**StatusDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-226">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**StatusDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-227">Contém indicadores do status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-227">Contains indicators of the current status of the element.</span></span> <span data-ttu-id="f2a6c-228">O primeiro valor da propriedade **OperationalStatus** deve conter o status principal do elemento.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-228">The first value of the **OperationalStatus** property should contain the primary status for the element.</span></span>

> [!Note]  
> <span data-ttu-id="f2a6c-229">A propriedade **OperationalStatus** substitui a propriedade de **status** preterida.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-229">The **OperationalStatus** property replaces the deprecated **Status** property.</span></span> <span data-ttu-id="f2a6c-230">Devido ao uso generalizado da propriedade **status** existente em aplicativos de gerenciamento, é altamente recomendável que os provedores ou a instrumentação forneçam as propriedades **status** e **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f2a6c-230">Due to the widespread use of the existing **Status** property in management applications, we strongly recommend that providers or instrumentation provide both the **Status** and **OperationalStatus** properties.</span></span> <span data-ttu-id="f2a6c-231">Quando instrumentado, **status**, porque é uma propriedade de valor único, também deve fornecer o status principal do elemento.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-231">When instrumented, **Status**, because it is a single-valued property, should also provide the primary status of the element.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2a6c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f2a6c-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f2a6c-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f2a6c-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (3)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f2a6c-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (4)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-237">O elemento está funcionando, mas precisa de atenção.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-237">The element is functioning, but needs attention.</span></span> <span data-ttu-id="f2a6c-238">Exemplos de Estados "sob estresse" são sobrecarga, superaquecido e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-238">Examples of "Stressed" states are overload, overheated, and so on.</span></span>

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="f2a6c-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (5)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-240">Um elemento está funcionando nominalmente, mas prevendo uma falha em um futuro próximo.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-240">An element is functioning nominally but predicting a failure in the near future.</span></span>

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f2a6c-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (6)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="f2a6c-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (7)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f2a6c-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (8)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f2a6c-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (9)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="f2a6c-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (10)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-246">Ocorreu uma parada ordenada.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-246">An orderly stop has occurred.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="f2a6c-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (11)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-248">Um elemento que está sendo configurado, mantido, limpo ou administrado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-248">An element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f2a6c-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sem contato** (12)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-250">O sistema de monitoramento tem conhecimento desse elemento, mas nunca foi capaz de estabelecer comunicações com ele.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-250">The monitoring system has knowledge of this element, but has never been able to establish communications with it.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="f2a6c-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-252">O elemento ManagedSystem é conhecido por existir e foi contatado com êxito no passado, mas está inacessível no momento.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-252">The ManagedSystem Element is known to exist and has been contacted successfully in the past, but is currently unreachable.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="f2a6c-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (14)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-254">Uma parada abrupta, onde o estado e a configuração do elemento talvez precisem ser atualizados, ocorreu.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-254">An abrupt stop, where where the state and configuration of the element might need to be updated, has occurred.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="f2a6c-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (15)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-256">O elemento está inativo ou desativado.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-256">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="f2a6c-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (16)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-258">Esse elemento pode ser "OK", mas outro elemento, no qual ele é dependente, está em erro.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-258">This element might be "OK" but that another element, on which it is dependent, is in error.</span></span> <span data-ttu-id="f2a6c-259">Um exemplo é um serviço de rede ou ponto de extremidade que não pode funcionar devido a problemas de rede de camada inferior.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-259">An example is a network service or endpoint that cannot function due to lower-layer networking problems.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="f2a6c-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (17)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-261">O elemento concluiu sua operação.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-261">The element has completed its operation.</span></span>

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span data-ttu-id="f2a6c-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Modo de energia** (18)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Power Mode** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f2a6c-263">O elemento tem informações adicionais do modelo de energia contidas na associação PowerManagementService associada.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-263">The element has additional power model information contained in the Associated PowerManagementService association.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f2a6c-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f2a6c-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2a6c-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-269">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**DetailedStatus**","**CIM \_ ManagedSystemElement**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-269">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**DetailedStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-270">Indica um valor de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-270">Indicates a high-level status value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f2a6c-271">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-271">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f2a6c-272">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-272">**OK** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f2a6c-273">**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-273">**Degraded** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f2a6c-274">**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-274">**Error** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f2a6c-275">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-275">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f2a6c-276">**Fornecedor reservado** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-276">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2a6c-277">**Status**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-277">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-280">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ ManagedSystemElement**.**OperationalStatus**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f2a6c-280">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-281">Indica o status principal do objeto.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-281">Indicates the primary status of the object.</span></span>

> [!Note]  
> <span data-ttu-id="f2a6c-282">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-282">This property is deprecated.</span></span> <span data-ttu-id="f2a6c-283">Ele é substituído pela propriedade **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f2a6c-283">It is replaced by the **OperationalStatus** property.</span></span> <span data-ttu-id="f2a6c-284">Se você optar por usar a propriedade **status** para compatibilidade com versões anteriores, ela deverá ser secundária à propriedade **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f2a6c-284">If you choose to use the **Status** property for backward compatibility, it should be secondary to the **OperationalStatus** property.</span></span>

 

<dt>



 <span data-ttu-id="f2a6c-285">("OK")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-285">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-286">("Erro")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-286">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-287">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-287">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-288">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-288">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-289">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-289">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-290">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-290">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-291">("Parando")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-291">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-292">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-292">("Service")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-293">("Sob estresse")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-293">("Stressed")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-294">("Recover")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-294">("NonRecover")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-295">("Sem contato")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-295">("No Contact")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-296">("Perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-296">("Lost Comm")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2a6c-297">("Parado")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-297">("Stopped")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2a6c-298">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-298">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6c-299">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2a6c-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6c-301">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM ManagedSystemElement**.**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="f2a6c-301">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="f2a6c-302">Indica as descrições dos valores correspondentes na matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f2a6c-302">Indicates descriptions of the corresponding values in the **OperationalStatus** array.</span></span> <span data-ttu-id="f2a6c-303">Por exemplo, se um elemento na propriedade **OperationalStatus** contiver o valor **parando**, o elemento no mesmo índice de matriz nessa propriedade poderá conter uma explicação sobre por que um objeto está sendo interrompido.</span><span class="sxs-lookup"><span data-stu-id="f2a6c-303">For example, if an element in the **OperationalStatus** property contains the value **Stopping**, then the element at the same array index in this property might contain an explanation as to why an object is being stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2a6c-304">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2a6c-304">Requirements</span></span>



| <span data-ttu-id="f2a6c-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2a6c-305">Requirement</span></span> | <span data-ttu-id="f2a6c-306">Valor</span><span class="sxs-lookup"><span data-stu-id="f2a6c-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a6c-307">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2a6c-307">Minimum supported client</span></span><br/> | <span data-ttu-id="f2a6c-308">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f2a6c-308">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f2a6c-309">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2a6c-309">Minimum supported server</span></span><br/> | <span data-ttu-id="f2a6c-310">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2a6c-310">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f2a6c-311">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2a6c-311">Namespace</span></span><br/>                | <span data-ttu-id="f2a6c-312">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f2a6c-312">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f2a6c-313">MOF</span><span class="sxs-lookup"><span data-stu-id="f2a6c-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2a6c-314"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2a6c-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2a6c-315">DLL</span><span class="sxs-lookup"><span data-stu-id="f2a6c-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2a6c-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2a6c-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2a6c-317">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2a6c-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a6c-318">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="f2a6c-318">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

