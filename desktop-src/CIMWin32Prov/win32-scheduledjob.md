---
description: Representa um trabalho criado com o comando AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010121"
---
# <a name="win32_scheduledjob-class"></a><span data-ttu-id="60c73-103">\_Classe Win32 ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="60c73-103">Win32\_ScheduledJob class</span></span>

<span data-ttu-id="60c73-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob do Win32**   representa um trabalho criado com o comando **at** .</span><span class="sxs-lookup"><span data-stu-id="60c73-104">The **Win32\_ScheduledJob** [WMI class](../wmisdk/retrieving-a-class.md) represents a job created with the **AT** command.</span></span>

> [!Note]  
> <span data-ttu-id="60c73-105">A classe **Win32 \_ ScheduledJob** não representa um trabalho criado com o assistente de tarefa agendada no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="60c73-105">The **Win32\_ScheduledJob** class does not represent a job created with the Scheduled Task Wizard from the Control Panel.</span></span> <span data-ttu-id="60c73-106">Você não pode alterar uma tarefa criada pelo WMI na interface do usuário de tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="60c73-106">You cannot change a task created by WMI in the Scheduled Tasks UI.</span></span> <span data-ttu-id="60c73-107">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="60c73-107">For more information, see the Remarks section.</span></span>

 

<span data-ttu-id="60c73-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="60c73-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="60c73-109">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="60c73-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c73-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60c73-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="60c73-111">Membros</span><span class="sxs-lookup"><span data-stu-id="60c73-111">Members</span></span>

<span data-ttu-id="60c73-112">A classe **Win32 \_ ScheduledJob** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="60c73-112">The **Win32\_ScheduledJob** class has these types of members:</span></span>

-   [<span data-ttu-id="60c73-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="60c73-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="60c73-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="60c73-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60c73-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="60c73-115">Methods</span></span>

<span data-ttu-id="60c73-116">A classe **Win32 \_ ScheduledJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="60c73-116">The **Win32\_ScheduledJob** class has these methods.</span></span>



| <span data-ttu-id="60c73-117">Método</span><span class="sxs-lookup"><span data-stu-id="60c73-117">Method</span></span>                                                      | <span data-ttu-id="60c73-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="60c73-118">Description</span></span>                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60c73-119">**Criada**</span><span class="sxs-lookup"><span data-stu-id="60c73-119">**Create**</span></span>](create-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="60c73-120">Método de classe que envia um trabalho para o sistema operacional para execução em uma data e hora futura especificadas.</span><span class="sxs-lookup"><span data-stu-id="60c73-120">Class method that submits a job to the operating system for execution at a specified future time and date.</span></span><br/> |
| [<span data-ttu-id="60c73-121">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="60c73-121">**Delete**</span></span>](delete-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="60c73-122">Método de classe que exclui um trabalho agendado.</span><span class="sxs-lookup"><span data-stu-id="60c73-122">Class method that deletes a scheduled job.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="60c73-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="60c73-123">Properties</span></span>

<span data-ttu-id="60c73-124">A classe **Win32 \_ ScheduledJob** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="60c73-124">The **Win32\_ScheduledJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60c73-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="60c73-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60c73-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-128">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="60c73-128">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-129">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="60c73-129">A short textual description of the object.</span></span>

<span data-ttu-id="60c73-130">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-131">**Comando**</span><span class="sxs-lookup"><span data-stu-id="60c73-131">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60c73-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-134">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**no comando \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| ")</span><span class="sxs-lookup"><span data-stu-id="60c73-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Command**")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-135">Nome do comando, programa em lotes ou arquivo binário (e argumentos de linha de comando) que o serviço de agendamento usa para invocar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="60c73-135">Name of the command, batch program, or binary file (and command-line arguments) that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="60c73-136">Exemplo: "**Defrag** **/q/f**"</span><span class="sxs-lookup"><span data-stu-id="60c73-136">Example: "**defrag** **/q/f**"</span></span>

</dd> <dt>

<span data-ttu-id="60c73-137">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="60c73-137">**DaysOfMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c73-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-140">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**no \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**")</span><span class="sxs-lookup"><span data-stu-id="60c73-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfMonth**")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-141">Dias do mês em que o trabalho está agendado para ser executado.</span><span class="sxs-lookup"><span data-stu-id="60c73-141">Days of the month when the job is scheduled to run.</span></span> <span data-ttu-id="60c73-142">Se um trabalho estiver agendado para ser executado em vários dias do mês, esses valores poderão ser Unidos em um OR lógico.</span><span class="sxs-lookup"><span data-stu-id="60c73-142">If a job is scheduled to run on multiple days of the month, these values can be joined in a logical OR.</span></span> <span data-ttu-id="60c73-143">Por exemplo, se um trabalho for executado no 1º e no 16º de cada mês, o valor da propriedade **DaysOfMonth** será 1 ou 32768.</span><span class="sxs-lookup"><span data-stu-id="60c73-143">For example, if a job is to run on the 1st and 16th of each month, the value of the **DaysOfMonth** property would be 1 OR 32768.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="60c73-144"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="60c73-144"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-145">primeiro</span><span class="sxs-lookup"><span data-stu-id="60c73-145">1st</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="60c73-146"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="60c73-146"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-147">2º</span><span class="sxs-lookup"><span data-stu-id="60c73-147">2nd</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="60c73-148"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="60c73-148"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-149">3a.</span><span class="sxs-lookup"><span data-stu-id="60c73-149">3rd</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="60c73-150"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="60c73-150"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-151">4a.</span><span class="sxs-lookup"><span data-stu-id="60c73-151">4th</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="60c73-152"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="60c73-152"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-153">5</span><span class="sxs-lookup"><span data-stu-id="60c73-153">5th</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="60c73-154"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="60c73-154"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-155">6</span><span class="sxs-lookup"><span data-stu-id="60c73-155">6th</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="60c73-156"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="60c73-156"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-157">07</span><span class="sxs-lookup"><span data-stu-id="60c73-157">7th</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="60c73-158"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="60c73-158"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-159">oitavo</span><span class="sxs-lookup"><span data-stu-id="60c73-159">8th</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="60c73-160"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="60c73-160"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-161">nono</span><span class="sxs-lookup"><span data-stu-id="60c73-161">9th</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="60c73-162"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="60c73-162"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-163">10º</span><span class="sxs-lookup"><span data-stu-id="60c73-163">10th</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="60c73-164"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="60c73-164"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-165">11º</span><span class="sxs-lookup"><span data-stu-id="60c73-165">11th</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="60c73-166"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="60c73-166"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-167">12º</span><span class="sxs-lookup"><span data-stu-id="60c73-167">12th</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="60c73-168"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="60c73-168"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-169">13º</span><span class="sxs-lookup"><span data-stu-id="60c73-169">13th</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="60c73-170"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="60c73-170"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-171">14</span><span class="sxs-lookup"><span data-stu-id="60c73-171">14th</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="60c73-172"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="60c73-172"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-173">15º</span><span class="sxs-lookup"><span data-stu-id="60c73-173">15th</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="60c73-174"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="60c73-174"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-175">16</span><span class="sxs-lookup"><span data-stu-id="60c73-175">16th</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="60c73-176"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="60c73-176"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-177">dia</span><span class="sxs-lookup"><span data-stu-id="60c73-177">17th</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="60c73-178"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="60c73-178"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-179">18</span><span class="sxs-lookup"><span data-stu-id="60c73-179">18th</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="60c73-180"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="60c73-180"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-181">décimo</span><span class="sxs-lookup"><span data-stu-id="60c73-181">19th</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="60c73-182"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="60c73-182"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-183">dia</span><span class="sxs-lookup"><span data-stu-id="60c73-183">20th</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="60c73-184"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="60c73-184"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-185">21º</span><span class="sxs-lookup"><span data-stu-id="60c73-185">21st</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="60c73-186"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="60c73-186"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-187">22º</span><span class="sxs-lookup"><span data-stu-id="60c73-187">22nd</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="60c73-188"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="60c73-188"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-189">23º</span><span class="sxs-lookup"><span data-stu-id="60c73-189">23rd</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="60c73-190"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="60c73-190"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-191">24</span><span class="sxs-lookup"><span data-stu-id="60c73-191">24th</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="60c73-192"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="60c73-192"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-193">25</span><span class="sxs-lookup"><span data-stu-id="60c73-193">25th</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="60c73-194"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="60c73-194"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-195">26</span><span class="sxs-lookup"><span data-stu-id="60c73-195">26th</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="60c73-196"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="60c73-196"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-197">27</span><span class="sxs-lookup"><span data-stu-id="60c73-197">27th</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="60c73-198"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="60c73-198"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-199">dia</span><span class="sxs-lookup"><span data-stu-id="60c73-199">28th</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="60c73-200"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="60c73-200"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-201">dia</span><span class="sxs-lookup"><span data-stu-id="60c73-201">29th</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="60c73-202"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="60c73-202"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-203">dia</span><span class="sxs-lookup"><span data-stu-id="60c73-203">30th</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="60c73-204"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="60c73-204"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="60c73-205">dia</span><span class="sxs-lookup"><span data-stu-id="60c73-205">31st</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="60c73-206">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="60c73-206">**DaysOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-207">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c73-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-209">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**em \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")</span><span class="sxs-lookup"><span data-stu-id="60c73-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfWeek**")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-210">Dias da semana em que um trabalho é agendado para execução.</span><span class="sxs-lookup"><span data-stu-id="60c73-210">Days of the week when a job is scheduled to run.</span></span> <span data-ttu-id="60c73-211">Se um trabalho estiver agendado para ser executado em vários dias da semana, os valores poderão ser Unidos em um OR lógico.</span><span class="sxs-lookup"><span data-stu-id="60c73-211">If a job is scheduled to run on multiple days of the week, the values can be joined in a logical OR.</span></span> <span data-ttu-id="60c73-212">Por exemplo, se um trabalho estiver agendado para ser executado em segundas, às quartas-e sextas-feiras, o valor da propriedade **DaysOfWeek** seria 1 ou 4 ou 16.</span><span class="sxs-lookup"><span data-stu-id="60c73-212">For example, if a job is scheduled to run on Mondays, Wednesdays, and Fridays the value of the **DaysOfWeek** property would be 1 OR 4 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="60c73-213">**Segunda** (1)</span><span class="sxs-lookup"><span data-stu-id="60c73-213">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="60c73-214">**Terça-feira** (2)</span><span class="sxs-lookup"><span data-stu-id="60c73-214">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="60c73-215">**Quarta-feira** (4)</span><span class="sxs-lookup"><span data-stu-id="60c73-215">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="60c73-216">**Quinta-feira** (8)</span><span class="sxs-lookup"><span data-stu-id="60c73-216">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="60c73-217">**Sexta-feira** (16)</span><span class="sxs-lookup"><span data-stu-id="60c73-217">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="60c73-218">**Sábado** (32)</span><span class="sxs-lookup"><span data-stu-id="60c73-218">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="60c73-219">**Domingo** (64)</span><span class="sxs-lookup"><span data-stu-id="60c73-219">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60c73-220">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="60c73-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60c73-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-223">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="60c73-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-224">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="60c73-224">A textual description of the object.</span></span>

<span data-ttu-id="60c73-225">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-226">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="60c73-226">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-227">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60c73-227">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c73-229">Período de tempo em que o trabalho foi executado.</span><span class="sxs-lookup"><span data-stu-id="60c73-229">Length of time the job has been executing.</span></span>

<span data-ttu-id="60c73-230">Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-230">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="60c73-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-232">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60c73-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-234">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="60c73-234">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-235">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="60c73-235">Indicates when the object was installed.</span></span> <span data-ttu-id="60c73-236">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="60c73-236">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="60c73-237">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-238">**InteractWithDesktop**</span><span class="sxs-lookup"><span data-stu-id="60c73-238">**InteractWithDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-239">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="60c73-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-241">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede do win32api \| [**no trabalho de sinalizadores de \_ informação**](/windows/win32/api/lmat/ns-lmat-at_info)não \|  \| **\_ interativa**")</span><span class="sxs-lookup"><span data-stu-id="60c73-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_NONINTERACTIVE**")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-242">O trabalho especificado é interativo, o que significa que um usuário pode fornecer entrada a um trabalho agendado enquanto ele está em execução.</span><span class="sxs-lookup"><span data-stu-id="60c73-242">Specified job is interactive, which means that a user can give input to a scheduled job while it is executing.</span></span>

</dd> <dt>

<span data-ttu-id="60c73-243">**JobId**</span><span class="sxs-lookup"><span data-stu-id="60c73-243">**JobId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-244">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c73-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-246">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede do win32api \| [**no \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**")</span><span class="sxs-lookup"><span data-stu-id="60c73-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobId**")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-247">Identificando o número do trabalho.</span><span class="sxs-lookup"><span data-stu-id="60c73-247">Identifying number of the job.</span></span> <span data-ttu-id="60c73-248">Ele é usado por métodos como um identificador para um trabalho que está sendo agendado neste computador.</span><span class="sxs-lookup"><span data-stu-id="60c73-248">It is used by methods as a handle to one job being scheduled on this computer.</span></span>

</dd> <dt>

<span data-ttu-id="60c73-249">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="60c73-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-250">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60c73-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-252">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**em sinalizador de \_ Enumeração**](/windows/win32/api/lmat/ns-lmat-at_enum) \|  \| **\_ \_ erro de exec de trabalho**")</span><span class="sxs-lookup"><span data-stu-id="60c73-252">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**Flags**\|**JOB\_EXEC\_ERROR**")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-253">Status da execução na última vez em que o trabalho foi agendado para execução.</span><span class="sxs-lookup"><span data-stu-id="60c73-253">Status of execution the last time this job was scheduled to run.</span></span>

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

<span data-ttu-id="60c73-254">**Êxito** ("êxito")</span><span class="sxs-lookup"><span data-stu-id="60c73-254">**Success** ("Success")</span></span>


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

<span data-ttu-id="60c73-255">**Falha** ("falha")</span><span class="sxs-lookup"><span data-stu-id="60c73-255">**Failure** ("Failure")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60c73-256">**Nome**</span><span class="sxs-lookup"><span data-stu-id="60c73-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60c73-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-259">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="60c73-259">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-260">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="60c73-260">Label by which the object is known.</span></span> <span data-ttu-id="60c73-261">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="60c73-261">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="60c73-262">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-263">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="60c73-263">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60c73-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c73-266">O usuário é notificado após a conclusão ou falha do trabalho.</span><span class="sxs-lookup"><span data-stu-id="60c73-266">User is notified upon job completion or failure.</span></span>

<span data-ttu-id="60c73-267">Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-267">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-268">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="60c73-268">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60c73-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c73-271">Usuário que enviou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="60c73-271">User who submitted the job.</span></span>

<span data-ttu-id="60c73-272">Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-272">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-273">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="60c73-273">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-274">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60c73-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c73-276">Importância da execução de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="60c73-276">Importance of a job's execution.</span></span>

<span data-ttu-id="60c73-277">Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-277">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-278">**RunRepeatedly**</span><span class="sxs-lookup"><span data-stu-id="60c73-278">**RunRepeatedly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-279">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="60c73-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-281">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede do win32api \| [**em \_ informações de**](/windows/win32/api/lmat/ns-lmat-at_info) \| **sinalizadores** de \| **trabalho são \_ executadas \_ periodicamente**")</span><span class="sxs-lookup"><span data-stu-id="60c73-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_RUN\_PERIODICALLY**")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-282">O trabalho agendado é executado repetidamente nos dias em que o trabalho é agendado.</span><span class="sxs-lookup"><span data-stu-id="60c73-282">Scheduled job runs repeatedly on the days that the job is scheduled.</span></span> <span data-ttu-id="60c73-283">Se for **false**, o trabalho será executado uma vez.</span><span class="sxs-lookup"><span data-stu-id="60c73-283">If **False**, then the job is run one time.</span></span>

</dd> <dt>

<span data-ttu-id="60c73-284">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="60c73-284">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-285">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60c73-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-287">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| estruturas de gerenciamento \| [**de rede em \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime**")</span><span class="sxs-lookup"><span data-stu-id="60c73-287">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobTime**")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-288">Hora UTC para executar o trabalho, na forma de "AAAAMMDDHHMMSS. MMMMMm (+-) OOO ", onde" aaaammdd "deve ser substituído por" \* \* \* \* \* \* \* \* ".</span><span class="sxs-lookup"><span data-stu-id="60c73-288">UTC time to run the job, in the form of "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="60c73-289">A substituição é necessária porque o serviço de agendamento só permite que os trabalhos sejam configurados para serem executados uma vez ou executados em um dia do mês ou da semana.</span><span class="sxs-lookup"><span data-stu-id="60c73-289">The replacement is necessary because the scheduling service only allows jobs to be configured to run one time, or run on a day of the month or week.</span></span> <span data-ttu-id="60c73-290">Um trabalho não pode ser executado em uma data específica.</span><span class="sxs-lookup"><span data-stu-id="60c73-290">A job cannot be run on a specific date.</span></span>

<span data-ttu-id="60c73-291">A seção "(+-) OOO" do valor da propriedade **StartTime** é a tendência atual para a conversão de hora local.</span><span class="sxs-lookup"><span data-stu-id="60c73-291">The "(+-)OOO" section of the **StartTime** property value is the current bias for local time translation.</span></span> <span data-ttu-id="60c73-292">A tendência é a diferença entre a hora UTC e a hora local.</span><span class="sxs-lookup"><span data-stu-id="60c73-292">The bias is the difference between the UTC time and local time.</span></span> <span data-ttu-id="60c73-293">Para calcular a tendência de seu fuso horário, multiplique o número de horas em que o fuso horário está adiantado ou atrasado no horário de Greenwich (GMT) por 60 (use um número positivo para o número de horas se o fuso horário estiver à frente do GMT e um número negativo se o fuso horário estiver atrás do GMT).</span><span class="sxs-lookup"><span data-stu-id="60c73-293">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="60c73-294">Adicione um 60 adicional ao seu cálculo se o seu fuso horário estiver usando o horário de verão.</span><span class="sxs-lookup"><span data-stu-id="60c73-294">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="60c73-295">Por exemplo, o fuso horário padrão do Pacífico é de oito horas atrás do GMT, portanto, a tendência é igual a-420 (-8 \* 60 + 60) quando o horário de verão está em uso e-480 (-8 \* 60) quando o horário de verão não está em uso.</span><span class="sxs-lookup"><span data-stu-id="60c73-295">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="60c73-296">Você também pode determinar o valor da tendência consultando a propriedade Bias da classe TimeZone do [**Win32 \_**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="60c73-296">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

<span data-ttu-id="60c73-297">Por exemplo: " \* \* \* \* \* \* \* \* 123000.000000-420" especifica 14,30 (2:30 P.M.) PST com o horário de verão em vigor.</span><span class="sxs-lookup"><span data-stu-id="60c73-297">For example: "\*\*\*\*\*\*\*\*123000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

</dd> <dt>

<span data-ttu-id="60c73-298">**Status**</span><span class="sxs-lookup"><span data-stu-id="60c73-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60c73-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c73-301">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="60c73-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="60c73-302">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="60c73-302">String that indicates the current status of the object.</span></span> <span data-ttu-id="60c73-303">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="60c73-303">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="60c73-304">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="60c73-304">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="60c73-305">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="60c73-305">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="60c73-306">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="60c73-306">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="60c73-307">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="60c73-307">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="60c73-308">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="60c73-308">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="60c73-309">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-309">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="60c73-310">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="60c73-310">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="60c73-311">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="60c73-311">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="60c73-312">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="60c73-312">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="60c73-313">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="60c73-313">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60c73-314">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="60c73-314">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="60c73-315">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="60c73-315">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="60c73-316">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="60c73-316">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="60c73-317">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="60c73-317">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="60c73-318">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="60c73-318">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="60c73-319">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="60c73-319">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="60c73-320">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="60c73-320">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="60c73-321">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="60c73-321">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="60c73-322">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="60c73-322">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60c73-323">**Timeenvio**</span><span class="sxs-lookup"><span data-stu-id="60c73-323">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-324">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60c73-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c73-326">Hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="60c73-326">Time that the job was submitted.</span></span>

<span data-ttu-id="60c73-327">Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-327">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="60c73-328">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="60c73-328">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c73-329">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60c73-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60c73-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60c73-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c73-331">Hora em que o trabalho é inválido ou deve ser parado.</span><span class="sxs-lookup"><span data-stu-id="60c73-331">Time at which the job is invalid or should be stopped.</span></span>

<span data-ttu-id="60c73-332">Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-332">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60c73-333">Comentários</span><span class="sxs-lookup"><span data-stu-id="60c73-333">Remarks</span></span>

<span data-ttu-id="60c73-334">Cada trabalho agendado no serviço de agendamento é armazenado de forma persistente (o Agendador pode iniciar um trabalho após uma reinicialização) e é executado na hora e no dia da semana ou mês especificados.</span><span class="sxs-lookup"><span data-stu-id="60c73-334">Each job scheduled against the schedule service is stored persistently (the scheduler can start a job after a reboot), and is executed at the specified time and day of the week or month.</span></span> <span data-ttu-id="60c73-335">Se o computador não estiver ativo ou se o serviço agendado não estiver em execução na hora do trabalho especificado, o serviço de agendamento executará o trabalho especificado no dia seguinte no horário especificado.</span><span class="sxs-lookup"><span data-stu-id="60c73-335">If the computer is not active, or if the scheduled service is not running at the specified job time, the schedule service runs the specified job on the next day at the specified time.</span></span>

<span data-ttu-id="60c73-336">Os trabalhos são agendados de acordo com o tempo universal coordenado (UTC) com deslocamento de tendência de Greenwich Mean Time (GMT), o que significa que um trabalho pode ser especificado usando qualquer fuso horário.</span><span class="sxs-lookup"><span data-stu-id="60c73-336">Jobs are scheduled according to Coordinated Universal Time (UTC) with bias offset from Greenwich Mean Time (GMT), which means that a job can be specified using any time zone.</span></span> <span data-ttu-id="60c73-337">A classe **Win32 \_ ScheduledJob** retorna a hora local com o deslocamento UTC ao enumerar um objeto e converte para a hora local ao criar novos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="60c73-337">The **Win32\_ScheduledJob** class returns the local time with UTC offset when enumerating an object, and converts to local time when creating new jobs.</span></span> <span data-ttu-id="60c73-338">Por exemplo, um trabalho especificado para ser executado em um computador em Boston às 10:30 P.M.</span><span class="sxs-lookup"><span data-stu-id="60c73-338">For example, a job specified to run on a computer in Boston at 10:30 P.M.</span></span> <span data-ttu-id="60c73-339">A hora da segunda-feira PST será agendada para ser executada localmente às 1:30 da manhã</span><span class="sxs-lookup"><span data-stu-id="60c73-339">Monday PST time will be scheduled to run locally at 1:30 A.M.</span></span> <span data-ttu-id="60c73-340">EST de terça-feira.</span><span class="sxs-lookup"><span data-stu-id="60c73-340">Tuesday EST.</span></span>

> [!Note]  
> <span data-ttu-id="60c73-341">Um cliente deve levar em conta se o horário de verão está ou não em operação no computador local e, se for, subtrair uma tendência de 60 minutos do deslocamento UTC.</span><span class="sxs-lookup"><span data-stu-id="60c73-341">A client must take into account whether or not daylight savings time is in operation on the local computer, and if it is, then subtract a bias of 60 minutes from the UTC offset.</span></span>

 

<span data-ttu-id="60c73-342">A classe **Win32 \_ ScheduledJob** é derivada do [**\_ trabalho CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-342">The **Win32\_ScheduledJob** class is derived from [**CIM\_Job**](cim-job.md).</span></span> <span data-ttu-id="60c73-343">Você deve ser um membro do grupo Administradores para criar um trabalho agendado usando essa classe.</span><span class="sxs-lookup"><span data-stu-id="60c73-343">You must be a member of the administrators group to create a scheduled job using this class.</span></span>

<span data-ttu-id="60c73-344">A classe **Win32 \_ ScheduledJob** é internamente usando o protocolo at, que está associado ao reprovamento a partir do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="60c73-344">The **Win32\_ScheduledJob** class is internally using the AT protocol, which is bound to deprecation starting with Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="60c73-345">Como uma primeira etapa, o protocolo AT é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="60c73-345">As a first step the AT protocol is disabled by default.</span></span> <span data-ttu-id="60c73-346">Se o protocolo estiver desabilitado, por exemplo, chamar o método [**Create**](create-method-in-class-win32-scheduledjob.md) em um objeto **Win32 \_ ScheduledJob** falhará com o erro 0x8.</span><span class="sxs-lookup"><span data-stu-id="60c73-346">If the protocol is disabled, for example calling the [**Create**](create-method-in-class-win32-scheduledjob.md) method on a **Win32\_ScheduledJob** object will fail with error 0x8.</span></span> <span data-ttu-id="60c73-347">Você pode ativar o protocolo AT novamente adicionando a seguinte entrada de registro:</span><span class="sxs-lookup"><span data-stu-id="60c73-347">You can turn the AT protocol back on by adding the following registry entry:</span></span>

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

<span data-ttu-id="60c73-348">Talvez seja necessário reiniciar o computador para tornar a configuração eficaz.</span><span class="sxs-lookup"><span data-stu-id="60c73-348">You may need to restart the machine to make the setting effective.</span></span>

<span data-ttu-id="60c73-349">Como o **Win32 \_ ScheduledJob** é baseado na API Win32 do [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , você não pode usar essa classe em conjunto com o Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="60c73-349">Because **Win32\_ScheduledJob** is based on the [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) Win32 API, you cannot use this class in conjunction with the Task Scheduler.</span></span> <span data-ttu-id="60c73-350">Se você quiser usar Agendador de Tarefas, use a API Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="60c73-350">If you wish to use Task Scheduler, use the Task Scheduler API.</span></span> <span data-ttu-id="60c73-351">Para obter mais informações, consulte a [referência de Agendador de tarefas](../taskschd/task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="60c73-351">For more information, see the [Task Scheduler Reference](../taskschd/task-scheduler-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="60c73-352">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60c73-352">Examples</span></span>

<span data-ttu-id="60c73-353">O exemplo de código VBScript a seguir agenda Notepad.exe para ser executado interativamente às 1:25 pela hora do computador local todas as quartas-feiras.</span><span class="sxs-lookup"><span data-stu-id="60c73-353">The following VBScript code example schedules Notepad.exe to run interactively at 1:25 by the local computer time every Wednesday.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a><span data-ttu-id="60c73-354">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60c73-354">Requirements</span></span>



| <span data-ttu-id="60c73-355">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c73-355">Requirement</span></span> | <span data-ttu-id="60c73-356">Valor</span><span class="sxs-lookup"><span data-stu-id="60c73-356">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60c73-357">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60c73-357">Minimum supported client</span></span><br/> | <span data-ttu-id="60c73-358">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60c73-358">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60c73-359">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60c73-359">Minimum supported server</span></span><br/> | <span data-ttu-id="60c73-360">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60c73-360">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60c73-361">Namespace</span><span class="sxs-lookup"><span data-stu-id="60c73-361">Namespace</span></span><br/>                | <span data-ttu-id="60c73-362">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="60c73-362">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60c73-363">MOF</span><span class="sxs-lookup"><span data-stu-id="60c73-363">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60c73-364"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60c73-364"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60c73-365">DLL</span><span class="sxs-lookup"><span data-stu-id="60c73-365">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c73-366"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60c73-366"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c73-367">Confira também</span><span class="sxs-lookup"><span data-stu-id="60c73-367">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c73-368">**Trabalho do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="60c73-368">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dt>

[<span data-ttu-id="60c73-369">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="60c73-369">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="60c73-370">Tarefas do WMI: tarefas agendadas</span><span class="sxs-lookup"><span data-stu-id="60c73-370">WMI Tasks: Scheduled Tasks</span></span>](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
