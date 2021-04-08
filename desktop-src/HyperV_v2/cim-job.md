---
description: Um elemento lógico que representa uma unidade de trabalho a ser executada, como um script ou um trabalho de impressão. Um trabalho é diferente de um processo porque um trabalho pode ser agendado ou enfileirado e sua execução não está limitada a um único sistema.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: Classe CIM_Job (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922257"
---
# <a name="cim_job-class-hyper-v-management"></a><span data-ttu-id="ac429-104">Classe CIM_Job (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ac429-104">CIM_Job class (Hyper-V management)</span></span>

<span data-ttu-id="ac429-105">Um elemento lógico que representa uma unidade de trabalho a ser executada, como um script ou um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="ac429-105">A logical element that represents a unit of work to execute, such as a script or a print job.</span></span> <span data-ttu-id="ac429-106">Um trabalho é diferente de um processo porque um trabalho pode ser agendado ou enfileirado e sua execução não está limitada a um único sistema.</span><span class="sxs-lookup"><span data-stu-id="ac429-106">A job is distinct from a process because a job can be scheduled or queued, and its execution is not limited to a single system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac429-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac429-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a><span data-ttu-id="ac429-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ac429-108">Members</span></span>

<span data-ttu-id="ac429-109">A classe de **\_ trabalho CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ac429-109">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="ac429-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac429-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ac429-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac429-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ac429-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac429-112">Methods</span></span>

<span data-ttu-id="ac429-113">A classe de **\_ trabalho CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ac429-113">The **CIM\_Job** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="ac429-114">Método</span><span class="sxs-lookup"><span data-stu-id="ac429-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="ac429-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac429-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ac429-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span><span class="sxs-lookup"><span data-stu-id="ac429-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ac429-117">Esse método é preterido.</span><span class="sxs-lookup"><span data-stu-id="ac429-117">This method is deprecated.</span></span> <span data-ttu-id="ac429-118">Em vez disso, use o método <strong>RequestStateChange</strong> .</span><span class="sxs-lookup"><span data-stu-id="ac429-118">Instead, use the <strong>RequestStateChange</strong> method.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ac429-119">Descrição preterida: desliga um trabalho.</span><span class="sxs-lookup"><span data-stu-id="ac429-119">Deprecated description: Shuts down a job.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="ac429-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac429-120">Properties</span></span>

<span data-ttu-id="ac429-121">A classe de **\_ trabalho CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ac429-121">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac429-122">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="ac429-122">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-123">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ac429-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac429-125">**True** para excluir o trabalho após a conclusão; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ac429-125">**True** to delete the job upon completion; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="ac429-126">Essa propriedade não excluirá trabalhos concluídos antes que essa propriedade seja definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="ac429-126">This property will not delete jobs that complete before this property is set to **True**.</span></span>

 

</dd> <dt>

<span data-ttu-id="ac429-127">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-127">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-128">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac429-130">A duração pela qual o trabalho foi executado.</span><span class="sxs-lookup"><span data-stu-id="ac429-130">The duration for which the job has run.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-131">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ac429-131">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac429-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac429-134">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**ErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="ac429-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-135">Um código de erro específico do fornecedor que captura informações de processamento para trabalhos recorrentes.</span><span class="sxs-lookup"><span data-stu-id="ac429-135">A vendor-specific error code that captures processing information for recurring jobs.</span></span> <span data-ttu-id="ac429-136">O valor deve ser definido como zero se o trabalho for concluído sem erros.</span><span class="sxs-lookup"><span data-stu-id="ac429-136">The value must be set to zero if the job completed without error.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-137">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ac429-137">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac429-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac429-140">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="ac429-140">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-141">Uma cadeia de caracteres de forma livre que contém uma descrição do código de erro correspondente na propriedade **ErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="ac429-141">A free-form string that contains a description of the corresponding error code in the **ErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-142">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="ac429-142">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac429-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac429-145">O número de vezes para executar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ac429-145">The number of times to run the job.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-146">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="ac429-146">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac429-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac429-149">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="ac429-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-150">Uma cadeia de caracteres de forma livre que representa o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ac429-150">A free-form string that represents the status of the job.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-151">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-151">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-152">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac429-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac429-154">Indica se os horários nas propriedades **RunStartInterval** e **UntilTime** representam horários locais ou horários UTC.</span><span class="sxs-lookup"><span data-stu-id="ac429-154">Indicates whether the times in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

<span data-ttu-id="ac429-155">**Hora local** (1)</span><span class="sxs-lookup"><span data-stu-id="ac429-155">**Local Time** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

<span data-ttu-id="ac429-156">**Hora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="ac429-156">**UTC Time** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac429-157">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="ac429-157">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac429-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac429-160">O usuário para notificar quando um trabalho for concluído ou falhar.</span><span class="sxs-lookup"><span data-stu-id="ac429-160">The user to notify when a job completes or fails.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-161">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="ac429-161">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac429-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac429-164">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**Recoveryaction**")</span><span class="sxs-lookup"><span data-stu-id="ac429-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-165">Uma cadeia de caracteres que descreve a ação de recuperação quando a propriedade **recoveryaction** é **outra** ("1").</span><span class="sxs-lookup"><span data-stu-id="ac429-165">A string that describes the recovery action when the **RecoveryAction** property is **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="ac429-166">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="ac429-166">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac429-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac429-169">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")</span><span class="sxs-lookup"><span data-stu-id="ac429-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OwningJobElement**](cim-owningjobelement.md).")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-170">O usuário que enviou o trabalho ou o nome do serviço ou do método que solicitou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ac429-170">The user that submitted the Job, or the service or method name that requested the job.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-171">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="ac429-171">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-172">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac429-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac429-174">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("porcentagem")</span><span class="sxs-lookup"><span data-stu-id="ac429-174">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-175">A porcentagem do trabalho concluído.</span><span class="sxs-lookup"><span data-stu-id="ac429-175">The percentage of the job that is complete.</span></span>

> [!Note]  
> <span data-ttu-id="ac429-176">O valor "101" é indefinido e não será permitido na próxima revisão principal da especificação.</span><span class="sxs-lookup"><span data-stu-id="ac429-176">The value "101" is undefined and will be not be allowed in the next major revision of the specification.</span></span>

 

</dd> <dt>

<span data-ttu-id="ac429-177">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="ac429-177">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-178">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac429-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac429-180">A importância do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ac429-180">The importance of the job.</span></span> <span data-ttu-id="ac429-181">Quanto menor o número, maior a prioridade.</span><span class="sxs-lookup"><span data-stu-id="ac429-181">The lower the number, the higher the priority.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-182">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="ac429-182">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-183">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac429-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac429-185">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**OtherRecoveryAction**")</span><span class="sxs-lookup"><span data-stu-id="ac429-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**OtherRecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-186">Descreve a ação de recuperação a ser tomada quando um trabalho de execução falha.</span><span class="sxs-lookup"><span data-stu-id="ac429-186">Describes the recovery action to take when a run job fails.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac429-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="ac429-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ac429-188">É desconhecido quanto à ação de recuperação a ser tomada.</span><span class="sxs-lookup"><span data-stu-id="ac429-188">It is unknown as to what recovery action to take.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ac429-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ac429-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ac429-190">A ação de recuperação será especificada na propriedade **OtherRecoveryAction** .</span><span class="sxs-lookup"><span data-stu-id="ac429-190">The recovery action will be specified in the **OtherRecoveryAction** property.</span></span>

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span data-ttu-id="ac429-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>Não **continuar** (2)</span><span class="sxs-lookup"><span data-stu-id="ac429-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ac429-192">Pare a execução do trabalho e atualize adequadamente seu status.</span><span class="sxs-lookup"><span data-stu-id="ac429-192">Stop the execution of the job and appropriately update its status.</span></span>

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span data-ttu-id="ac429-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar com o próximo trabalho** (3)</span><span class="sxs-lookup"><span data-stu-id="ac429-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ac429-194">Continue com o próximo trabalho na fila.</span><span class="sxs-lookup"><span data-stu-id="ac429-194">Continue with the next job in the queue.</span></span>

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span data-ttu-id="ac429-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Executar trabalho novamente** (4)</span><span class="sxs-lookup"><span data-stu-id="ac429-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ac429-196">O trabalho deve ser executado novamente.</span><span class="sxs-lookup"><span data-stu-id="ac429-196">The job should be re-run.</span></span>

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span data-ttu-id="ac429-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Executar trabalho de recuperação** (5)</span><span class="sxs-lookup"><span data-stu-id="ac429-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Run Recovery Job** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ac429-198">Execute o trabalho associado usando a relação **RecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="ac429-198">Run the Job associated using the **RecoveryJob** relationship.</span></span> <span data-ttu-id="ac429-199">Observe que o trabalho de recuperação já deve estar na fila na qual ele será executado.</span><span class="sxs-lookup"><span data-stu-id="ac429-199">Note that the recovery Job must already be in the queue from which it will run.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ac429-200">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="ac429-200">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-201">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="ac429-201">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ac429-203">Qualificadores: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**RunMonth**","**\_ trabalho CIM**.**RunDayOfWeek**","**\_ trabalho CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="ac429-203">Qualifiers: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-204">Um inteiro que é usado em conjunto com a propriedade **RunDayOfWeek** para indicar o dia em que o trabalho é processado; ou, se **RunDayOfWeek** for definido como zero, **RunDay** indicará o dia do mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="ac429-204">An integer that is used on conjunction with the **RunDayOfWeek** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span> <span data-ttu-id="ac429-205">Se **RunDay** for um inteiro negativo, ele especificará um dia em relação ao fim do mês, ou se **RunDay** for um inteiro positivo, ele especificará um dia relativo ao início do mês.</span><span class="sxs-lookup"><span data-stu-id="ac429-205">If **RunDay** is a negative integer, it specifies a day relative to the end of the month, or if **RunDay** is a positive integer, it specifies a day relative to the beginning of the month.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-206">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="ac429-206">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-207">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="ac429-207">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-208">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ac429-209">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**RunMonth**","**\_ trabalho CIM**.**RunDay**","**\_ trabalho CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="ac429-209">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-210">Um inteiro que é usado em conjunto com a propriedade **RunDay** para indicar o dia em que o trabalho é processado; ou, se **RunDayOfWeek** for definido como zero, **RunDay** indicará o dia do mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="ac429-210">An integer that is used on conjunction with the **RunDay** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span>

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

<span data-ttu-id="ac429-211">**-Sábado** (-7)</span><span class="sxs-lookup"><span data-stu-id="ac429-211">**-Saturday** (-7)</span></span>


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

<span data-ttu-id="ac429-212">**-Sexta** (-6)</span><span class="sxs-lookup"><span data-stu-id="ac429-212">**-Friday** (-6)</span></span>


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

<span data-ttu-id="ac429-213">**-Quinta-feira** (-5)</span><span class="sxs-lookup"><span data-stu-id="ac429-213">**-Thursday** (-5)</span></span>


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

<span data-ttu-id="ac429-214">**-Quartas** (-4)</span><span class="sxs-lookup"><span data-stu-id="ac429-214">**-Wednesday** (-4)</span></span>


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

<span data-ttu-id="ac429-215">**-Terça-feira** (-3)</span><span class="sxs-lookup"><span data-stu-id="ac429-215">**-Tuesday** (-3)</span></span>


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

<span data-ttu-id="ac429-216">**-Segunda-feira** (-2)</span><span class="sxs-lookup"><span data-stu-id="ac429-216">**-Monday** (-2)</span></span>


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

<span data-ttu-id="ac429-217">**-Domingo** (-1)</span><span class="sxs-lookup"><span data-stu-id="ac429-217">**-Sunday** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

<span data-ttu-id="ac429-218">**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="ac429-218">**ExactDayOfMonth** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="ac429-219">**Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="ac429-219">**Sunday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="ac429-220">**Segunda** (2)</span><span class="sxs-lookup"><span data-stu-id="ac429-220">**Monday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="ac429-221">**Terça-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="ac429-221">**Tuesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="ac429-222">**Quarta-feira** (4)</span><span class="sxs-lookup"><span data-stu-id="ac429-222">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="ac429-223">**Quinta-feira** (5)</span><span class="sxs-lookup"><span data-stu-id="ac429-223">**Thursday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="ac429-224">**Sexta-feira** (6)</span><span class="sxs-lookup"><span data-stu-id="ac429-224">**Friday** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="ac429-225">**Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="ac429-225">**Saturday** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac429-226">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="ac429-226">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-227">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="ac429-227">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-228">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ac429-229">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**RunDay**","**\_ trabalho CIM**.**RunDayOfWeek**","**\_ trabalho CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="ac429-229">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-230">O mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="ac429-230">The month when the job is processed.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="ac429-231">**Janeiro** (0)</span><span class="sxs-lookup"><span data-stu-id="ac429-231">**January** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="ac429-232">**Fevereiro** (1)</span><span class="sxs-lookup"><span data-stu-id="ac429-232">**February** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="ac429-233">**Março** (2)</span><span class="sxs-lookup"><span data-stu-id="ac429-233">**March** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="ac429-234">**Abril** (3)</span><span class="sxs-lookup"><span data-stu-id="ac429-234">**April** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="ac429-235">**Maio** (4)</span><span class="sxs-lookup"><span data-stu-id="ac429-235">**May** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="ac429-236">**Junho** (5)</span><span class="sxs-lookup"><span data-stu-id="ac429-236">**June** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="ac429-237">**Julho** (6)</span><span class="sxs-lookup"><span data-stu-id="ac429-237">**July** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="ac429-238">**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="ac429-238">**August** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="ac429-239">**Setembro** (8)</span><span class="sxs-lookup"><span data-stu-id="ac429-239">**September** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="ac429-240">**Outubro** (9)</span><span class="sxs-lookup"><span data-stu-id="ac429-240">**October** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="ac429-241">**Novembro** (10)</span><span class="sxs-lookup"><span data-stu-id="ac429-241">**November** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="ac429-242">**Dezembro** (11)</span><span class="sxs-lookup"><span data-stu-id="ac429-242">**December** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac429-243">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="ac429-243">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-244">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-244">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-245">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ac429-246">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**RunMonth**","**\_ trabalho CIM**.**RunDay**","**\_ trabalho CIM**.**RunDayOfWeek**","**\_ trabalho CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="ac429-246">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-247">O intervalo de tempo após a meia-noite quando o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="ac429-247">The time interval after midnight when the job is be processed.</span></span> <span data-ttu-id="ac429-248">Por exemplo, "00000000020000.000000:000" indica que o trabalho é executado em ou após duas horas locais, ou hora UTC (UTC é especificado com a propriedade **LocalOrUtcTime** ).</span><span class="sxs-lookup"><span data-stu-id="ac429-248">For example, "00000000020000.000000:000" indicates that the job is be run on or after two o'clock local time, or UTC time (UTC is specified with the **LocalOrUtcTime** property).</span></span>

</dd> <dt>

<span data-ttu-id="ac429-249">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-249">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-250">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-251">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-251">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ac429-252">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (**" \_ trabalho CIM**.**RunMonth**","**\_ trabalho CIM**.**RunDay**","**\_ trabalho CIM**.**RunDayOfWeek**","**\_ trabalho CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="ac429-252">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="ac429-253">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="ac429-253">This property is deprecated.</span></span> <span data-ttu-id="ac429-254">Em vez disso, recomendamos que você use as propriedades **RunMonth**, **RunDay**, **RunDayOfWeek** e **RunStartInterval** .</span><span class="sxs-lookup"><span data-stu-id="ac429-254">Instead we recommend that you use the **RunMonth**, **RunDay**, **RunDayOfWeek**, and **RunStartInterval** properties.</span></span>

 

<span data-ttu-id="ac429-255">A hora em que o trabalho atual é agendado para iniciar.</span><span class="sxs-lookup"><span data-stu-id="ac429-255">The time when the current job is scheduled to start.</span></span> <span data-ttu-id="ac429-256">Esse tempo pode ser representado por uma data e hora ou um intervalo relativo à hora em que a propriedade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="ac429-256">This time can be represented by a date and time, or an interval relative to the time when the property is requested.</span></span> <span data-ttu-id="ac429-257">Um valor de todos os zeros indica que o trabalho já está em execução.</span><span class="sxs-lookup"><span data-stu-id="ac429-257">A value of all zeroes indicates that the job is already executing.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-258">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-258">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-259">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac429-261">A hora em que o trabalho foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ac429-261">The time when the job started.</span></span> <span data-ttu-id="ac429-262">Esse tempo pode ser representado por uma data e hora ou por um intervalo relativo à hora em que a propriedade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="ac429-262">This time can be represented by a date and time, or by an interval relative to the time when the property is requested.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-263">**Timeenvio**</span><span class="sxs-lookup"><span data-stu-id="ac429-263">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-264">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-264">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac429-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac429-266">A hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="ac429-266">The time when the job was submitted.</span></span> <span data-ttu-id="ac429-267">Um valor de todos os zeros indica que o elemento pai não é capaz de relatar uma data e hora.</span><span class="sxs-lookup"><span data-stu-id="ac429-267">A value of all zeroes indicates that the parent element is not capable of reporting a date and time.</span></span>

</dd> <dt>

<span data-ttu-id="ac429-268">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-268">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac429-269">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac429-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac429-270">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ac429-270">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ac429-271">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**LocalOrUtcTime**")</span><span class="sxs-lookup"><span data-stu-id="ac429-271">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**LocalOrUtcTime**")</span></span>
</dt> </dl>

<span data-ttu-id="ac429-272">O tempo após o qual o trabalho se torna inválido ou deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="ac429-272">The time after which the job becomes invalid or should be stopped.</span></span> <span data-ttu-id="ac429-273">A hora pode ser representada por uma data e hora ou por um intervalo relativo à hora em que essa propriedade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="ac429-273">The time can be represented by a date and time, or by an interval relative to the time when this property is requested.</span></span> <span data-ttu-id="ac429-274">Um valor de todos os noves indica que o trabalho pode ser executado indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="ac429-274">A value of all nines indicates that the job can run indefinitely.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac429-275">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac429-275">Requirements</span></span>



| <span data-ttu-id="ac429-276">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac429-276">Requirement</span></span> | <span data-ttu-id="ac429-277">Valor</span><span class="sxs-lookup"><span data-stu-id="ac429-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac429-278">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac429-278">Minimum supported client</span></span><br/> | <span data-ttu-id="ac429-279">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ac429-279">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ac429-280">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac429-280">Minimum supported server</span></span><br/> | <span data-ttu-id="ac429-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac429-281">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ac429-282">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac429-282">Namespace</span></span><br/>                | <span data-ttu-id="ac429-283">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ac429-283">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ac429-284">MOF</span><span class="sxs-lookup"><span data-stu-id="ac429-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac429-285"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac429-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac429-286">DLL</span><span class="sxs-lookup"><span data-stu-id="ac429-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac429-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac429-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac429-288">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac429-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac429-289">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="ac429-289">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

