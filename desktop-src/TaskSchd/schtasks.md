---
title: Schtasks.exe
description: Permite que um administrador crie, exclua, consulte, altere, execute e Finalize tarefas agendadas em um computador local ou remoto.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Agendador de Tarefas
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1c9ba2c13053a8c550128f5d66623b5eed3a9dec
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314629"
---
# <a name="schtasksexe"></a><span data-ttu-id="0897f-104">Schtasks.exe</span><span class="sxs-lookup"><span data-stu-id="0897f-104">Schtasks.exe</span></span>

<span data-ttu-id="0897f-105">Permite que um administrador crie, exclua, consulte, altere, execute e Finalize tarefas agendadas em um computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="0897f-105">Enables an administrator to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> <span data-ttu-id="0897f-106">A execução de Schtasks.exe sem argumentos exibe o status e a próxima hora de execução para cada tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="0897f-106">Running Schtasks.exe without arguments displays the status and next run time for each registered task.</span></span> 

<span data-ttu-id="0897f-107">Para obter mais informações sobre Agendador de Tarefas, consulte esta introdução: [Agendador de tarefas para desenvolvedores](task-scheduler-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="0897f-107">For more information on Task Scheduler, see this introduction: [Task Scheduler for developers](task-scheduler-start-page.md).</span></span>

## <a name="creating-a-task"></a><span data-ttu-id="0897f-108">Criando uma tarefa</span><span class="sxs-lookup"><span data-stu-id="0897f-108">Creating a Task</span></span>

<span data-ttu-id="0897f-109">A sintaxe a seguir é usada para criar uma tarefa no computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="0897f-109">The following syntax is used to create a task on the local or remote computer.</span></span>

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a><span data-ttu-id="0897f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0897f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0897f-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="0897f-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-112">Um valor que especifica o computador remoto ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="0897f-112">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="0897f-113">Se omitido, o parâmetro do sistema usa como padrão o computador local.</span><span class="sxs-lookup"><span data-stu-id="0897f-113">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome de usuário**</span><span class="sxs-lookup"><span data-stu-id="0897f-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-115">Um valor que especifica o contexto de usuário no qual Schtasks.exe deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="0897f-115">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ senha \]**</span><span class="sxs-lookup"><span data-stu-id="0897f-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-117">Um valor que especifica a senha para um determinado contexto de usuário.</span><span class="sxs-lookup"><span data-stu-id="0897f-117">A value that specifies the password for a given user context.</span></span> <span data-ttu-id="0897f-118">Se for omitido, Schtasks.exe solicitará a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="0897f-118">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/Ru** **nome_usuário**</span><span class="sxs-lookup"><span data-stu-id="0897f-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-120">Um valor que especifica o contexto de usuário no qual a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-120">A value that specifies the user context under which the task runs.</span></span> <span data-ttu-id="0897f-121">Para a conta do sistema, os valores válidos são "", "NT AUTHORITY \\ System" ou "System".</span><span class="sxs-lookup"><span data-stu-id="0897f-121">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="0897f-122">Para Agendador de Tarefas tarefas 2,0, "NT AUTHORITY \\ LocalService" e "NT Authority \\ NetworkService" também são valores válidos.</span><span class="sxs-lookup"><span data-stu-id="0897f-122">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE", and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[ senha \]**</span><span class="sxs-lookup"><span data-stu-id="0897f-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-124">Um valor que especifica a senha para o usuário especificado com o parâmetro/RU.</span><span class="sxs-lookup"><span data-stu-id="0897f-124">A value that specifies the password for the user specified with the /RU parameter.</span></span> <span data-ttu-id="0897f-125">Para solicitar a senha, o valor deve ser " \* " ou nenhum valor.</span><span class="sxs-lookup"><span data-stu-id="0897f-125">To prompt for the password, the value must be either "\*" or no value.</span></span> <span data-ttu-id="0897f-126">Essa senha é ignorada para a conta do sistema.</span><span class="sxs-lookup"><span data-stu-id="0897f-126">This password is ignored for the system account.</span></span> <span data-ttu-id="0897f-127">Esse parâmetro deve ser combinado com a opção/RU ou/XML.</span><span class="sxs-lookup"><span data-stu-id="0897f-127">This parameter must be combined with either /RU or the /XML switch.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span> **Agenda** de/SC</span><span class="sxs-lookup"><span data-stu-id="0897f-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **schedule**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-129">Um valor que especifica a frequência de agendamento.</span><span class="sxs-lookup"><span data-stu-id="0897f-129">A value that specifies the schedule frequency.</span></span> <span data-ttu-id="0897f-130">Os valores válidos são: minuto, por hora, diariamente, SEMANAlmente, mensal, uma vez, onloginn, ONIDLE e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-130">Valid values are: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span> **Modificador** de/mo</span><span class="sxs-lookup"><span data-stu-id="0897f-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/MO** **modifier**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-132">Um valor que restringe o tipo de agendamento para permitir um controle mais preciso sobre a recorrência da agenda.</span><span class="sxs-lookup"><span data-stu-id="0897f-132">A value that refines the schedule type to allow for finer control over the schedule recurrence.</span></span> <span data-ttu-id="0897f-133">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0897f-133">Valid values are:</span></span>

-   <span data-ttu-id="0897f-134">MINUTO: 1-1439 minutos.</span><span class="sxs-lookup"><span data-stu-id="0897f-134">MINUTE: 1 - 1439 minutes.</span></span>
-   <span data-ttu-id="0897f-135">Por hora: 1-23 horas.</span><span class="sxs-lookup"><span data-stu-id="0897f-135">HOURLY: 1 - 23 hours.</span></span>
-   <span data-ttu-id="0897f-136">DIARIAMENTE: 1-365 dias.</span><span class="sxs-lookup"><span data-stu-id="0897f-136">DAILY: 1 - 365 days.</span></span>
-   <span data-ttu-id="0897f-137">SEMANAL: semanas de 1-52.</span><span class="sxs-lookup"><span data-stu-id="0897f-137">WEEKLY: weeks 1 - 52.</span></span>
-   <span data-ttu-id="0897f-138">UMA vez: nenhum modificador.</span><span class="sxs-lookup"><span data-stu-id="0897f-138">ONCE: No modifiers.</span></span>
-   <span data-ttu-id="0897f-139">OnStart: não há modificadores.</span><span class="sxs-lookup"><span data-stu-id="0897f-139">ONSTART: No modifiers.</span></span>
-   <span data-ttu-id="0897f-140">Onloginn: nenhum modificador.</span><span class="sxs-lookup"><span data-stu-id="0897f-140">ONLOGON: No modifiers.</span></span>
-   <span data-ttu-id="0897f-141">ONIDLE: nenhum modificador.</span><span class="sxs-lookup"><span data-stu-id="0897f-141">ONIDLE: No modifiers.</span></span>
-   <span data-ttu-id="0897f-142">MENSALmente: 1-12, ou primeiro, segundo, terceiro, quarto, último e LASTDAY.</span><span class="sxs-lookup"><span data-stu-id="0897f-142">MONTHLY: 1 - 12, or FIRST, SECOND, THIRD, FOURTH, LAST, and LASTDAY.</span></span>
-   <span data-ttu-id="0897f-143">OnEvent: cadeia de consulta de evento XPath.</span><span class="sxs-lookup"><span data-stu-id="0897f-143">ONEVENT: XPath event query string.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **dias**</span><span class="sxs-lookup"><span data-stu-id="0897f-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **days**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-145">Um valor que especifica o dia da semana para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-145">A value that specifies the day of the week to run the task.</span></span> <span data-ttu-id="0897f-146">Os valores válidos são: MON, terça-feira, qui, Sex, SAT, sol e para agendas mensais 1-31 (dias do mês).</span><span class="sxs-lookup"><span data-stu-id="0897f-146">Valid values are: MON, TUE, WED, THU, FRI, SAT, SUN and for MONTHLY schedules 1 - 31 (days of the month).</span></span> <span data-ttu-id="0897f-147">O caractere curinga ( \* ) especifica todos os dias.</span><span class="sxs-lookup"><span data-stu-id="0897f-147">The wildcard character (\*) specifies all days.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **meses**</span><span class="sxs-lookup"><span data-stu-id="0897f-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **months**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-149">Um valor que especifica os meses do ano.</span><span class="sxs-lookup"><span data-stu-id="0897f-149">A value that specifies months of the year.</span></span> <span data-ttu-id="0897f-150">O padrão é o primeiro dia do mês.</span><span class="sxs-lookup"><span data-stu-id="0897f-150">Defaults to the first day of the month.</span></span> <span data-ttu-id="0897f-151">Os valores válidos são: JAN, Fev, MAR, abr, maio, JUN, JUL, ago, SEP, OCT, NOV e DEC.</span><span class="sxs-lookup"><span data-stu-id="0897f-151">Valid values are: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV, and DEC.</span></span> <span data-ttu-id="0897f-152">O caractere curinga ( \* ) especifica todos os meses.</span><span class="sxs-lookup"><span data-stu-id="0897f-152">The wildcard character (\*) specifies all months.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **ociosotime**</span><span class="sxs-lookup"><span data-stu-id="0897f-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-154">Um valor que especifica a quantidade de tempo ocioso a aguardar antes de executar uma tarefa ONIDLE agendada.</span><span class="sxs-lookup"><span data-stu-id="0897f-154">A value that specifies the amount of idle time to wait before running a scheduled ONIDLE task.</span></span> <span data-ttu-id="0897f-155">O intervalo válido é de 1-999 minutos.</span><span class="sxs-lookup"><span data-stu-id="0897f-155">The valid range is 1 - 999 minutes.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Nome_Tarefa**</span><span class="sxs-lookup"><span data-stu-id="0897f-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-157">Um valor que especifica um nome que identifica exclusivamente a tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="0897f-157">A value that specifies a name which uniquely identifies the scheduled task.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span><span class="sxs-lookup"><span data-stu-id="0897f-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-159">Um valor que especifica o caminho e o nome do arquivo da tarefa a ser executada no horário agendado.</span><span class="sxs-lookup"><span data-stu-id="0897f-159">A value that specifies the path and file name of the task to be run at the scheduled time.</span></span> <span data-ttu-id="0897f-160">Por exemplo: C: \\ Windows \\ System32 \\calc.exe.</span><span class="sxs-lookup"><span data-stu-id="0897f-160">For example: C:\\Windows\\System32\\calc.exe.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="0897f-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-162">Um valor que especifica a hora de início para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-162">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="0897f-163">O formato de hora é HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="0897f-163">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="0897f-164">Por exemplo, 14:30 especifica 2: às 16h30.</span><span class="sxs-lookup"><span data-stu-id="0897f-164">For example, 14:30 specifies 2:30PM.</span></span> <span data-ttu-id="0897f-165">O padrão é a hora atual,/ST não é especificado.</span><span class="sxs-lookup"><span data-stu-id="0897f-165">The default is the current time is /ST is not specified.</span></span> <span data-ttu-id="0897f-166">Essa opção é necessária para Wit o argumento/SC ONCE.</span><span class="sxs-lookup"><span data-stu-id="0897f-166">This option is required wit the /SC ONCE argument.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/Ri** **intervalo**</span><span class="sxs-lookup"><span data-stu-id="0897f-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-168">Um valor que especifica o intervalo de repetição em minutos.</span><span class="sxs-lookup"><span data-stu-id="0897f-168">A value that specifies the repetition interval in minutes.</span></span> <span data-ttu-id="0897f-169">Isso não é aplicável para os seguintes tipos de agendamento: minuto, hora, OnStart, ONLOGON, ONIDLE e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-169">This is not applicable for the following schedule types: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="0897f-170">O intervalo válido é de 1-599940 minutos.</span><span class="sxs-lookup"><span data-stu-id="0897f-170">The valid range is 1 - 599940 minutes.</span></span> <span data-ttu-id="0897f-171">Se os parâmetros/ET ou/DU forem especificados, o padrão será 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="0897f-171">If either the /ET or /DU parameters are specified, the default is 10 minutes.</span></span>

<span data-ttu-id="0897f-172">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-172">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**</span><span class="sxs-lookup"><span data-stu-id="0897f-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-174">Um valor que especifica a hora de término para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-174">A value that specifies the end time to run the task.</span></span> <span data-ttu-id="0897f-175">O formato de hora é HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="0897f-175">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="0897f-176">Por exemplo, 14:50 especifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="0897f-176">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="0897f-177">Isso não é aplicável para os seguintes tipos de agendamento: OnStart, onloginn, ONIDLE e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-177">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

<span data-ttu-id="0897f-178">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-178">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **duração**</span><span class="sxs-lookup"><span data-stu-id="0897f-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-180">Um valor que especifica a duração da execução da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-180">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="0897f-181">O formato de hora é HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="0897f-181">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="0897f-182">Por exemplo, 14:50 especifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="0897f-182">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="0897f-183">Isso não é aplicável com/ET e para os seguintes tipos de agendamento: OnStart, onloginn, ONIDLE e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-183">This is not applicable with /ET and for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="0897f-184">Para tarefas/V1 (Agendador de Tarefas tarefas 1,0), se/RI for especificado, o padrão de duração será de uma hora.</span><span class="sxs-lookup"><span data-stu-id="0897f-184">For /V1 tasks (Task Scheduler 1.0 tasks), if /RI is specified, then the duration default is one hour.</span></span>

<span data-ttu-id="0897f-185">**Windows XP:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-185">**Windows XP:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="0897f-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-187">Um valor que termina a tarefa na hora de término ou no tempo de duração.</span><span class="sxs-lookup"><span data-stu-id="0897f-187">A value that terminates the task at the end time or duration time.</span></span> <span data-ttu-id="0897f-188">Isso não é aplicável para os seguintes tipos de agendamento: OnStart, onloginn, ONIDLE e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-188">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="0897f-189">A opção/ET ou/DU deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="0897f-189">Either /ET or /DU must be specified.</span></span>

<span data-ttu-id="0897f-190">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-190">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**</span><span class="sxs-lookup"><span data-stu-id="0897f-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-192">Um valor que especifica a primeira data na qual executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-192">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="0897f-193">O formato é mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="0897f-193">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="0897f-194">Esse valor usa como padrão a data atual.</span><span class="sxs-lookup"><span data-stu-id="0897f-194">This value defaults to the current date.</span></span> <span data-ttu-id="0897f-195">Isso não é aplicável aos seguintes tipos de agendamento: uma vez, OnStart, onloginn, ONIDLE e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-195">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="0897f-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-197">Um valor que especifica a última data em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-197">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="0897f-198">O formato é mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="0897f-198">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="0897f-199">Isso não é aplicável aos seguintes tipos de agendamento: uma vez, OnStart, onloginn, ONIDLE e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-199">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span><span class="sxs-lookup"><span data-stu-id="0897f-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-201">Um valor que especifica o canal de evento para gatilhos OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-201">A value that specifies the event channel for ONEVENT triggers.</span></span>

<span data-ttu-id="0897f-202">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-202">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="0897f-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-204">Um valor que permite que a tarefa seja executada interativamente somente se o usuário/RU estiver conectado no momento no momento em que a tarefa for executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-204">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="0897f-205">A tarefa será executada somente se o usuário estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="0897f-205">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="0897f-206">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-206">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span><span class="sxs-lookup"><span data-stu-id="0897f-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-208">Um valor que indica que nenhuma senha está armazenada.</span><span class="sxs-lookup"><span data-stu-id="0897f-208">A value that indicates that no password is stored.</span></span> <span data-ttu-id="0897f-209">A tarefa não é executada interativamente como o usuário fornecido.</span><span class="sxs-lookup"><span data-stu-id="0897f-209">The task does not run interactively as the given user.</span></span> <span data-ttu-id="0897f-210">Somente recursos locais estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0897f-210">Only local resources are available.</span></span>

<span data-ttu-id="0897f-211">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-211">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="0897f-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-213">Um valor que marca a tarefa a ser excluída após sua execução final.</span><span class="sxs-lookup"><span data-stu-id="0897f-213">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="0897f-214">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-214">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>Xmlfile do **/XML** </span><span class="sxs-lookup"><span data-stu-id="0897f-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-216">Um valor que cria uma tarefa a partir de um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="0897f-216">A value that creates a task from an XML file.</span></span> <span data-ttu-id="0897f-217">Esse parâmetro pode ser combinado com as opções/RU e/RP, ou com a opção/RP sozinha quando o XML da tarefa já contém a entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="0897f-217">This parameter can be combined with /RU and /RP switches, or with the /RP switch alone when the task XML already contains the principal.</span></span>

<span data-ttu-id="0897f-218">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-218">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span><span class="sxs-lookup"><span data-stu-id="0897f-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-220">Um valor que cria uma tarefa visível para as plataformas Windows 2000, Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0897f-220">A value that creates a task visible to Windows 2000, Windows Server 2003, and Windows XP platforms.</span></span>

<span data-ttu-id="0897f-221">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-221">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-222"><span id="_F_"></span><span id="_f_"></span>**F**</span><span class="sxs-lookup"><span data-stu-id="0897f-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-223">Um valor que força a criação da tarefa e suprime avisos se a tarefa especificada já existir.</span><span class="sxs-lookup"><span data-stu-id="0897f-223">A value that forcefully creates the task and suppresses warnings if the specified task already exists.</span></span>

<span data-ttu-id="0897f-224">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-224">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Nível** de/RL</span><span class="sxs-lookup"><span data-stu-id="0897f-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-226">Um valor que define o nível de execução para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-226">A value that sets the run level for the task.</span></span> <span data-ttu-id="0897f-227">Os valores válidos são limitado e mais alto.</span><span class="sxs-lookup"><span data-stu-id="0897f-227">Valid values are LIMITED and HIGHEST.</span></span> <span data-ttu-id="0897f-228">O padrão é limitado.</span><span class="sxs-lookup"><span data-stu-id="0897f-228">The default is LIMITED.</span></span>

<span data-ttu-id="0897f-229">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-229">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**</span><span class="sxs-lookup"><span data-stu-id="0897f-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-231">Um valor que especifica o tempo de espera para atrasar a tarefa depois que o gatilho é acionado.</span><span class="sxs-lookup"><span data-stu-id="0897f-231">A value that specifies the wait time to delay the task after the trigger is fired.</span></span> <span data-ttu-id="0897f-232">O formato de hora é mmmm: SS.</span><span class="sxs-lookup"><span data-stu-id="0897f-232">The time format is mmmm:ss.</span></span> <span data-ttu-id="0897f-233">Essa opção só é válida para os tipos de agendamento OnStart, ONLOGON e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-233">This option is only valid for schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="0897f-234">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-234">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-235"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="0897f-235"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-236">Um valor que exibe a mensagem de ajuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="0897f-236">A value that displays the help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0897f-237">Comentários</span><span class="sxs-lookup"><span data-stu-id="0897f-237">Remarks</span></span>

<span data-ttu-id="0897f-238">Ao criar uma tarefa em um computador remoto em execução no sistema operacional Windows XP, Windows Server 2003 ou Windows 2000, use a opção/v1</span><span class="sxs-lookup"><span data-stu-id="0897f-238">When creating a task on a remote computer running on the Windows XP, Windows Server 2003, or Windows 2000 operating system, use the /V1 switch.</span></span>

<span data-ttu-id="0897f-239">Não é possível criar uma tarefa remota de Agendador de Tarefas 1,0 não interativa (crie uma tarefa não usando a opção/IT e usando a opção/v1) se o computador remoto tiver a exceção de firewall de compartilhamento de arquivos e impressoras habilitada e a exceção de firewall de gerenciamento de tarefas agendadas remotas estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0897f-239">You cannot create a non-interactive remote Task Scheduler 1.0 task (create a task by not using the /IT switch and using the /V1 switch) if the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled.</span></span>

## <a name="deleting-a-task"></a><span data-ttu-id="0897f-240">Excluindo uma tarefa</span><span class="sxs-lookup"><span data-stu-id="0897f-240">Deleting a Task</span></span>

<span data-ttu-id="0897f-241">A sintaxe a seguir é usada para excluir uma ou mais tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="0897f-241">The following syntax is used to delete one or more scheduled tasks.</span></span>

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a><span data-ttu-id="0897f-242">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0897f-242">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0897f-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="0897f-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-244">Um valor que especifica o computador remoto ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="0897f-244">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="0897f-245">Se omitido, o parâmetro do sistema usa como padrão o computador local.</span><span class="sxs-lookup"><span data-stu-id="0897f-245">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome de usuário**</span><span class="sxs-lookup"><span data-stu-id="0897f-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-247">Um valor que especifica o contexto de usuário no qual Schtasks.exe deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="0897f-247">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ senha \]**</span><span class="sxs-lookup"><span data-stu-id="0897f-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-249">Um valor que especifica a senha para o contexto de usuário fornecido.</span><span class="sxs-lookup"><span data-stu-id="0897f-249">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="0897f-250">Se for omitido, Schtasks.exe solicitará a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="0897f-250">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Nome_Tarefa**</span><span class="sxs-lookup"><span data-stu-id="0897f-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-252">Um valor que especifica o nome da tarefa agendada a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="0897f-252">A value that specifies the name of the scheduled task to delete.</span></span> <span data-ttu-id="0897f-253">O caractere curinga ( \* ) pode ser usado para excluir todas as tarefas.</span><span class="sxs-lookup"><span data-stu-id="0897f-253">The wildcard character (\*) can be used to delete all tasks.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-254"><span id="_F_"></span><span id="_f_"></span>**F**</span><span class="sxs-lookup"><span data-stu-id="0897f-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-255">Um valor que força a exclusão da tarefa e suprime avisos se a tarefa especificada estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="0897f-255">A value that forcefully deletes the task and suppresses warnings if the specified task is running.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-256"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="0897f-256"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-257">Um valor que exibe a ajuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="0897f-257">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="running-a-task"></a><span data-ttu-id="0897f-258">Executando uma tarefa</span><span class="sxs-lookup"><span data-stu-id="0897f-258">Running a Task</span></span>

<span data-ttu-id="0897f-259">A sintaxe a seguir é usada para executar imediatamente uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="0897f-259">The following syntax is used to immediately run a scheduled task.</span></span>

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a><span data-ttu-id="0897f-260">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0897f-260">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0897f-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="0897f-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-262">Um valor que especifica o computador remoto ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="0897f-262">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="0897f-263">Se omitido, o parâmetro do sistema usa como padrão o computador local.</span><span class="sxs-lookup"><span data-stu-id="0897f-263">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome de usuário**</span><span class="sxs-lookup"><span data-stu-id="0897f-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-265">Um valor que especifica o contexto de usuário no qual Schtasks.exe deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="0897f-265">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ senha \]**</span><span class="sxs-lookup"><span data-stu-id="0897f-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-267">Um valor que especifica a senha para o contexto de usuário fornecido.</span><span class="sxs-lookup"><span data-stu-id="0897f-267">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="0897f-268">Se for omitido, Schtasks.exe solicitará a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="0897f-268">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Nome_Tarefa**</span><span class="sxs-lookup"><span data-stu-id="0897f-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-270">Um valor que especifica o nome da tarefa agendada a ser executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-270">A value that specifies the name of the scheduled task to run.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-271"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="0897f-271"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-272">Um valor que exibe a ajuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="0897f-272">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="ending-a-running-task"></a><span data-ttu-id="0897f-273">Finalizando uma tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="0897f-273">Ending a Running Task</span></span>

<span data-ttu-id="0897f-274">A sintaxe a seguir é usada para interromper uma tarefa agendada em execução.</span><span class="sxs-lookup"><span data-stu-id="0897f-274">The following syntax is used to stop a running scheduled task.</span></span>

> [!Note]  
> <span data-ttu-id="0897f-275">Para interromper a execução de uma tarefa remota, certifique-se de que o computador remoto tenha o compartilhamento de arquivos e impressoras e as exceções de firewall de gerenciamento de tarefas agendadas remotas habilitadas.</span><span class="sxs-lookup"><span data-stu-id="0897f-275">To stop a remote task from running, ensure that the remote computer has the File and Printer Sharing and Remote Scheduled Tasks Management firewall exceptions enabled.</span></span>

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a><span data-ttu-id="0897f-276">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0897f-276">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0897f-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="0897f-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-278">Um valor que especifica o computador remoto ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="0897f-278">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="0897f-279">Se omitido, o parâmetro do sistema usa como padrão o computador local.</span><span class="sxs-lookup"><span data-stu-id="0897f-279">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome de usuário**</span><span class="sxs-lookup"><span data-stu-id="0897f-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-281">Um valor que especifica o contexto de usuário no qual Schtasks.exe deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="0897f-281">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ senha \]**</span><span class="sxs-lookup"><span data-stu-id="0897f-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-283">Um valor que especifica a senha para o contexto de usuário fornecido.</span><span class="sxs-lookup"><span data-stu-id="0897f-283">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="0897f-284">Se for omitido, Schtasks.exe solicitará a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="0897f-284">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Nome_Tarefa**</span><span class="sxs-lookup"><span data-stu-id="0897f-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-286">Um valor que especifica o nome da tarefa agendada a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="0897f-286">A value that specifies the name of the scheduled task to stop.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-287"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="0897f-287"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-288">Um valor que exibe a ajuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="0897f-288">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="querying-for-task-information"></a><span data-ttu-id="0897f-289">Consultando informações sobre tarefas</span><span class="sxs-lookup"><span data-stu-id="0897f-289">Querying for Task Information</span></span>

<span data-ttu-id="0897f-290">A sintaxe a seguir é usada para exibir as tarefas agendadas do computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="0897f-290">The following syntax is used to display the scheduled tasks from the local or remote computer.</span></span>

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a><span data-ttu-id="0897f-291">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0897f-291">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0897f-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="0897f-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-293">Um valor que especifica o computador remoto ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="0897f-293">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="0897f-294">Se omitido, o parâmetro do sistema usa como padrão o computador local.</span><span class="sxs-lookup"><span data-stu-id="0897f-294">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome de usuário**</span><span class="sxs-lookup"><span data-stu-id="0897f-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-296">Um valor que especifica o contexto de usuário no qual Schtasks.exe deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="0897f-296">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ senha \]**</span><span class="sxs-lookup"><span data-stu-id="0897f-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-298">Um valor que especifica a senha para o contexto de usuário fornecido.</span><span class="sxs-lookup"><span data-stu-id="0897f-298">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="0897f-299">Se for omitido, Schtasks.exe solicitará a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="0897f-299">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/Fo** **formato**</span><span class="sxs-lookup"><span data-stu-id="0897f-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-301">Um valor que especifica o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="0897f-301">A value that specifies the output format.</span></span> <span data-ttu-id="0897f-302">Os valores válidos são tabela, lista e CSV.</span><span class="sxs-lookup"><span data-stu-id="0897f-302">The valid values are TABLE, LIST, and CSV.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span><span class="sxs-lookup"><span data-stu-id="0897f-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-304">Um valor que especifica que o cabeçalho da coluna não deve ser exibido na saída.</span><span class="sxs-lookup"><span data-stu-id="0897f-304">A value that specifies that the column header should not be displayed in the output.</span></span> <span data-ttu-id="0897f-305">Isso é válido somente para formatos de tabela e CSV.</span><span class="sxs-lookup"><span data-stu-id="0897f-305">This is valid only for TABLE and CSV formats.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="0897f-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-307">Um valor que exibe a saída de tarefa detalhada.</span><span class="sxs-lookup"><span data-stu-id="0897f-307">A value that displays verbose task output.</span></span>

> [!Note]  
> <span data-ttu-id="0897f-308">Se uma tarefa foi agendada para ser executada apenas uma vez, as informações de agendamento exibidas são "os dados de agendamento não estão disponíveis neste formato".</span><span class="sxs-lookup"><span data-stu-id="0897f-308">If a task was scheduled to run only one time, then the displayed schedule information is "Scheduling data is not available in this format."</span></span>

 

</dd> <dt>

<span data-ttu-id="0897f-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Nome_Tarefa**</span><span class="sxs-lookup"><span data-stu-id="0897f-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-310">Um valor que especifica o nome da tarefa para a qual recuperar as informações.</span><span class="sxs-lookup"><span data-stu-id="0897f-310">A value that specifies the task name for which to retrieve the information.</span></span> <span data-ttu-id="0897f-311">Se nenhum nome de tarefa for especificado, as informações para todas as tarefas serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="0897f-311">If no task name is specified, then information for all the tasks will be displayed.</span></span>

<span data-ttu-id="0897f-312">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-312">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span><span class="sxs-lookup"><span data-stu-id="0897f-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-314">Um valor que é usado para exibir as definições de tarefa em formato XML.</span><span class="sxs-lookup"><span data-stu-id="0897f-314">A value that is used to display the task definitions in XML format.</span></span>

<span data-ttu-id="0897f-315">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-315">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-316"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="0897f-316"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-317">Um valor que é usado para exibir a ajuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="0897f-317">A value that is used to display the Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="changing-a-task"></a><span data-ttu-id="0897f-318">Alterando uma tarefa</span><span class="sxs-lookup"><span data-stu-id="0897f-318">Changing a Task</span></span>

<span data-ttu-id="0897f-319">A sintaxe a seguir é usada para alterar a forma como o programa é executado, ou alterar a conta de usuário e a senha usadas por uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="0897f-319">The following syntax is used to change how the program runs, or change the user account and password used by a scheduled task.</span></span>

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a><span data-ttu-id="0897f-320">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0897f-320">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0897f-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="0897f-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-322">Um valor que especifica o computador remoto ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="0897f-322">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="0897f-323">Se omitido, o parâmetro do sistema usa como padrão o computador local.</span><span class="sxs-lookup"><span data-stu-id="0897f-323">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome de usuário**</span><span class="sxs-lookup"><span data-stu-id="0897f-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-325">Um valor que especifica o contexto de usuário no qual Schtasks.exe deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="0897f-325">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ senha \]**</span><span class="sxs-lookup"><span data-stu-id="0897f-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-327">Um valor que especifica a senha para o contexto de usuário fornecido.</span><span class="sxs-lookup"><span data-stu-id="0897f-327">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="0897f-328">Se for omitido, Schtasks.exe solicitará a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="0897f-328">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Nome_Tarefa**</span><span class="sxs-lookup"><span data-stu-id="0897f-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-330">Um valor que especifica qual tarefa agendada deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="0897f-330">A value that specifies which scheduled task to change.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru** **runasuser**</span><span class="sxs-lookup"><span data-stu-id="0897f-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-332">Um valor que altera o nome de usuário (contexto do usuário) no qual a tarefa agendada será executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-332">A value that changes the user name (user context) under which the scheduled task will run.</span></span> <span data-ttu-id="0897f-333">Para a conta do sistema, os valores válidos são "", "NT AUTHORITY \\ System" ou "System".</span><span class="sxs-lookup"><span data-stu-id="0897f-333">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="0897f-334">Para Agendador de Tarefas tarefas 2,0, "NT AUTHORITY \\ LocalService" e "NT Authority \\ NetworkService" também são valores válidos.</span><span class="sxs-lookup"><span data-stu-id="0897f-334">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE" and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span><span class="sxs-lookup"><span data-stu-id="0897f-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-336">Um valor que especifica uma nova senha para o contexto de usuário existente ou a senha para uma nova conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="0897f-336">A value that specifies a new password for the existing user context or the password for a new user account.</span></span> <span data-ttu-id="0897f-337">Essa senha é ignorada para a conta do sistema.</span><span class="sxs-lookup"><span data-stu-id="0897f-337">This password is ignored for the system account.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span><span class="sxs-lookup"><span data-stu-id="0897f-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-339">Um valor que especifica um novo programa em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-339">A value that specifies a new program that the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="0897f-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-341">Um valor que especifica a hora de início para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-341">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="0897f-342">O formato de hora é HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="0897f-342">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="0897f-343">Por exemplo, 14:30 especifica 2: às 16h30.</span><span class="sxs-lookup"><span data-stu-id="0897f-343">For example, 14:30 specifies 2:30PM.</span></span>

<span data-ttu-id="0897f-344">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-344">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/Ri** **intervalo**</span><span class="sxs-lookup"><span data-stu-id="0897f-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-346">Um valor que especifica o intervalo de repetição, em minutos.</span><span class="sxs-lookup"><span data-stu-id="0897f-346">A value that specifies the repetition interval, in minutes.</span></span> <span data-ttu-id="0897f-347">O intervalo válido é de 1-599940 minutos.</span><span class="sxs-lookup"><span data-stu-id="0897f-347">The valid range is 1 - 599940 minutes.</span></span>

<span data-ttu-id="0897f-348">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-348">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**</span><span class="sxs-lookup"><span data-stu-id="0897f-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-350">Um valor que especifica a hora de término da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-350">A value that specifies the end time for the task.</span></span> <span data-ttu-id="0897f-351">O formato de hora é HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="0897f-351">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="0897f-352">Por exemplo, 14:50 especifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="0897f-352">For example, 14:50 specifies 2:50PM.</span></span>

<span data-ttu-id="0897f-353">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-353">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **duração**</span><span class="sxs-lookup"><span data-stu-id="0897f-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-355">Um valor que especifica a duração da execução da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-355">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="0897f-356">O formato de hora é HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="0897f-356">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="0897f-357">Por exemplo, 14:50 especifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="0897f-357">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="0897f-358">Isso não é aplicável com o parâmetro/ET.</span><span class="sxs-lookup"><span data-stu-id="0897f-358">This is not applicable with the /ET parameter.</span></span>

<span data-ttu-id="0897f-359">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-359">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="0897f-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-361">Um valor que termina a tarefa na hora de término ou no tempo de duração.</span><span class="sxs-lookup"><span data-stu-id="0897f-361">A value that terminates the task at the end time or duration time.</span></span>

<span data-ttu-id="0897f-362">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-362">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**</span><span class="sxs-lookup"><span data-stu-id="0897f-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-364">Um valor que especifica a primeira data na qual executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-364">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="0897f-365">O formato é mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="0897f-365">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="0897f-366">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-366">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="0897f-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-368">Um valor que especifica a última data em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-368">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="0897f-369">O formato é mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="0897f-369">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="0897f-370">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-370">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="0897f-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-372">Um valor que permite que a tarefa seja executada interativamente somente se o usuário/RU estiver conectado no momento no momento em que a tarefa for executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-372">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="0897f-373">A tarefa será executada somente se o usuário estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="0897f-373">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="0897f-374">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-374">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Nível** de/RL</span><span class="sxs-lookup"><span data-stu-id="0897f-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-376">Um valor que define o nível de execução para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0897f-376">A value that sets the run level for the task.</span></span> <span data-ttu-id="0897f-377">Os valores válidos são limitado e mais alto.</span><span class="sxs-lookup"><span data-stu-id="0897f-377">Valid values are LIMITED and HIGHEST.</span></span>

<span data-ttu-id="0897f-378">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-378">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span><span class="sxs-lookup"><span data-stu-id="0897f-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-380">Um valor que habilita a tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="0897f-380">A value that enables the scheduled task.</span></span> <span data-ttu-id="0897f-381">Uma tarefa habilitada pode ser executada e uma tarefa desabilitada não pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="0897f-381">An enabled task can run, and a disabled task cannot run.</span></span>

<span data-ttu-id="0897f-382">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-382">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span><span class="sxs-lookup"><span data-stu-id="0897f-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-384">Um valor que desabilita a execução da tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="0897f-384">A value that disables the scheduled task from running.</span></span>

> [!Note]  
> <span data-ttu-id="0897f-385">Se uma tarefa remota Agendador de Tarefas 1,0 for desabilitada por Schtasks.exe e o computador remoto tiver a exceção de firewall de compartilhamento de arquivos e impressoras habilitada e a exceção de firewall de gerenciamento de tarefas agendadas remotas estiver desabilitada, a tarefa não será desabilitada quando lida de uma API Agendador de Tarefas 2,0.</span><span class="sxs-lookup"><span data-stu-id="0897f-385">If a remote Task Scheduler 1.0 task is disabled by Schtasks.exe and the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled, then the task will not be disabled when read from a Task Scheduler 2.0 API.</span></span>

 

<span data-ttu-id="0897f-386">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-386">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="0897f-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-388">Um valor que marca a tarefa a ser excluída após sua execução final.</span><span class="sxs-lookup"><span data-stu-id="0897f-388">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="0897f-389">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-389">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**</span><span class="sxs-lookup"><span data-stu-id="0897f-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="0897f-391">Um valor que especifica o tempo de espera para atrasar a execução da tarefa depois que o gatilho é acionado.</span><span class="sxs-lookup"><span data-stu-id="0897f-391">A value that specifies the wait time to delay the running of the task after the trigger is fired.</span></span> <span data-ttu-id="0897f-392">O formato de hora é mmmm: SS.</span><span class="sxs-lookup"><span data-stu-id="0897f-392">The time format is mmmm:ss.</span></span> <span data-ttu-id="0897f-393">Essa opção só é válida para tarefas com os tipos de agendamento OnStart, ONLOGON e OnEvent.</span><span class="sxs-lookup"><span data-stu-id="0897f-393">This option is only valid for tasks with the schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="0897f-394">**Windows XP e Windows Server 2003:** Esta opção não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0897f-394">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0897f-395"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="0897f-395"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="0897f-396">Um valor que exibe a mensagem de ajuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="0897f-396">A value that displays the Help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0897f-397">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0897f-397">Requirements</span></span>



| <span data-ttu-id="0897f-398">Requisito</span><span class="sxs-lookup"><span data-stu-id="0897f-398">Requirement</span></span> | <span data-ttu-id="0897f-399">Valor</span><span class="sxs-lookup"><span data-stu-id="0897f-399">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0897f-400">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0897f-400">Minimum supported client</span></span><br/> | <span data-ttu-id="0897f-401">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0897f-401">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0897f-402">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0897f-402">Minimum supported server</span></span><br/> | <span data-ttu-id="0897f-403">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0897f-403">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





