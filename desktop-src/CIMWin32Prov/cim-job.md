---
description: A \_ classe de trabalho CIM representa uma unidade de trabalho para um sistema, como um trabalho de impressão. Um trabalho é diferente de um processo porque um trabalho pode ser agendado.
ms.assetid: a689230e-2a62-4f0d-9961-9bbc055d3c6e
ms.tgt_platform: multiple
title: Classe CIM_Job (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.Caption
- CIM_Job.Description
- CIM_Job.InstallDate
- CIM_Job.Name
- CIM_Job.Status
- CIM_Job.ElapsedTime
- CIM_Job.JobStatus
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.StartTime
- CIM_Job.TimeSubmitted
- CIM_Job.UntilTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd527474309802a4c6d2315d8a9e61b6733e70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089274"
---
# <a name="cim_job-class-cimwin32-wmi-providers"></a><span data-ttu-id="e141b-104">Classe CIM_Job (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e141b-104">CIM_Job class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e141b-105">A classe de **\_ trabalho CIM** representa uma unidade de trabalho para um sistema, como um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="e141b-105">The **CIM\_Job** class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="e141b-106">Um trabalho é diferente de um processo porque um trabalho pode ser agendado.</span><span class="sxs-lookup"><span data-stu-id="e141b-106">A job is distinct from a process because a job can be scheduled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e141b-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e141b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e141b-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e141b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e141b-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e141b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e141b-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e141b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e141b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e141b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C564-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
};
```

## <a name="members"></a><span data-ttu-id="e141b-112">Membros</span><span class="sxs-lookup"><span data-stu-id="e141b-112">Members</span></span>

<span data-ttu-id="e141b-113">A classe de **\_ trabalho CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e141b-113">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="e141b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e141b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e141b-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e141b-115">Properties</span></span>

<span data-ttu-id="e141b-116">A classe de **\_ trabalho CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e141b-116">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e141b-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e141b-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e141b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e141b-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e141b-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e141b-121">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e141b-121">A short textual description of the object.</span></span>

<span data-ttu-id="e141b-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e141b-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e141b-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e141b-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e141b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e141b-126">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="e141b-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e141b-127">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e141b-127">A textual description of the object.</span></span>

<span data-ttu-id="e141b-128">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e141b-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e141b-129">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="e141b-129">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-130">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e141b-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e141b-132">Período de tempo em que o trabalho foi executado.</span><span class="sxs-lookup"><span data-stu-id="e141b-132">Length of time the job has been executing.</span></span>

</dd> <dt>

<span data-ttu-id="e141b-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e141b-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-134">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e141b-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e141b-136">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="e141b-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e141b-137">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e141b-137">Indicates when the object was installed.</span></span> <span data-ttu-id="e141b-138">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="e141b-138">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e141b-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e141b-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e141b-140">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="e141b-140">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e141b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e141b-143">Cadeia de caracteres de forma livre que representa o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e141b-143">Free-form string that represents the job status.</span></span>

</dd> <dt>

<span data-ttu-id="e141b-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e141b-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e141b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e141b-147">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e141b-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e141b-148">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e141b-148">Label by which the object is known.</span></span> <span data-ttu-id="e141b-149">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="e141b-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e141b-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e141b-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e141b-151">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="e141b-151">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e141b-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e141b-154">O usuário é notificado após a conclusão ou falha do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e141b-154">User is notified upon job completion or failure.</span></span>

</dd> <dt>

<span data-ttu-id="e141b-155">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="e141b-155">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e141b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e141b-158">Usuário que enviou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e141b-158">User who submitted the job.</span></span>

</dd> <dt>

<span data-ttu-id="e141b-159">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="e141b-159">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e141b-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e141b-162">Importância da execução de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="e141b-162">Importance of a job's execution.</span></span>

</dd> <dt>

<span data-ttu-id="e141b-163">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="e141b-163">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-164">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e141b-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e141b-166">Hora em que o trabalho começou.</span><span class="sxs-lookup"><span data-stu-id="e141b-166">Time that the job began.</span></span>

</dd> <dt>

<span data-ttu-id="e141b-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="e141b-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e141b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e141b-170">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e141b-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e141b-171">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e141b-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="e141b-172">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="e141b-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e141b-173">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="e141b-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e141b-174">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="e141b-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e141b-175">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="e141b-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e141b-176">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="e141b-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e141b-177">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="e141b-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e141b-178">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e141b-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e141b-179">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e141b-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e141b-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e141b-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e141b-181">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="e141b-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e141b-182">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e141b-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e141b-183">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e141b-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e141b-184">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e141b-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e141b-185">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e141b-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e141b-186">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="e141b-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e141b-187">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="e141b-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e141b-188">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="e141b-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e141b-189">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e141b-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e141b-190">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="e141b-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e141b-191">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="e141b-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e141b-192">**Timeenvio**</span><span class="sxs-lookup"><span data-stu-id="e141b-192">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-193">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e141b-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e141b-195">Hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="e141b-195">Time that the job was submitted.</span></span>

</dd> <dt>

<span data-ttu-id="e141b-196">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="e141b-196">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e141b-197">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e141b-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e141b-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e141b-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e141b-199">Hora em que o trabalho é inválido ou deve ser parado.</span><span class="sxs-lookup"><span data-stu-id="e141b-199">Time at which the job is invalid or should be stopped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e141b-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="e141b-200">Remarks</span></span>

<span data-ttu-id="e141b-201">A classe de **\_ trabalho CIM** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e141b-201">The **CIM\_Job** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="e141b-202">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e141b-202">WMI does not implement this class.</span></span> <span data-ttu-id="e141b-203">Para classes derivadas do **\_ trabalho CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e141b-203">For classes derived from **CIM\_Job**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e141b-204">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e141b-204">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e141b-205">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e141b-205">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e141b-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e141b-206">Requirements</span></span>



| <span data-ttu-id="e141b-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="e141b-207">Requirement</span></span> | <span data-ttu-id="e141b-208">Valor</span><span class="sxs-lookup"><span data-stu-id="e141b-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e141b-209">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e141b-209">Minimum supported client</span></span><br/> | <span data-ttu-id="e141b-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e141b-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e141b-211">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e141b-211">Minimum supported server</span></span><br/> | <span data-ttu-id="e141b-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e141b-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e141b-213">Namespace</span><span class="sxs-lookup"><span data-stu-id="e141b-213">Namespace</span></span><br/>                | <span data-ttu-id="e141b-214">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e141b-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e141b-215">MOF</span><span class="sxs-lookup"><span data-stu-id="e141b-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e141b-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e141b-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e141b-217">DLL</span><span class="sxs-lookup"><span data-stu-id="e141b-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e141b-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e141b-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e141b-219">Confira também</span><span class="sxs-lookup"><span data-stu-id="e141b-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e141b-220">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e141b-220">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

