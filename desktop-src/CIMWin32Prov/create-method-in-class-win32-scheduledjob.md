---
description: Envia um trabalho para um sistema operacional para execução em uma data e hora especificadas no futuro.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Método Create da classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296119"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="abda4-103">Método Create da classe Win32 \_ ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="abda4-103">Create method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="abda4-104">O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) envia um trabalho para um sistema operacional para execução em uma data e hora especificadas no futuro.</span><span class="sxs-lookup"><span data-stu-id="abda4-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method submits a job to an operating system for execution at a specified time and date in the future.</span></span> <span data-ttu-id="abda4-105">Esse método requer que o serviço de agendamento seja iniciado no computador para o qual o trabalho é enviado.</span><span class="sxs-lookup"><span data-stu-id="abda4-105">This method requires that the schedule service be started on the computer to which the job is submitted.</span></span>

<span data-ttu-id="abda4-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="abda4-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="abda4-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="abda4-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="abda4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abda4-108">Syntax</span></span>


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a><span data-ttu-id="abda4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abda4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abda4-110">*Comando* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abda4-110">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abda4-111">Nome do comando, programa em lotes ou arquivo binário e parâmetros de linha de comando que o serviço de agendamento usa para invocar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="abda4-111">Name of the command, batch program, or binary file and command-line parameters that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="abda4-112">Exemplo: "Defrag/q/f".</span><span class="sxs-lookup"><span data-stu-id="abda4-112">Example: "defrag /q /f".</span></span>

</dd> <dt>

<span data-ttu-id="abda4-113">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abda4-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abda4-114">Tempo universal coordenado (UTC) para executar um trabalho.</span><span class="sxs-lookup"><span data-stu-id="abda4-114">Coordinated Universal Time (UTC) time to run a job.</span></span> <span data-ttu-id="abda4-115">O formulário deve ser: "AAAAMMDDHHMMSS. MMMMMm (+-) OOO ", onde" aaaammdd "deve ser substituído por" \* \* \* \* \* \* \* \* ".</span><span class="sxs-lookup"><span data-stu-id="abda4-115">The form must be: "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="abda4-116">Por exemplo: " \* \* \* \* \* \* \* \* 143000.000000-420" especifica 14,30 (2:30 P.M.) PST com o horário de verão em vigor.</span><span class="sxs-lookup"><span data-stu-id="abda4-116">For example: "\*\*\*\*\*\*\*\*143000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

<span data-ttu-id="abda4-117">A seção "(+-) OOO" do valor da Propriedade StartTime é a tendência atual para a conversão de hora local.</span><span class="sxs-lookup"><span data-stu-id="abda4-117">The "(+-)OOO" section of the StartTime property value is the current bias for local time translation.</span></span> <span data-ttu-id="abda4-118">A tendência é a diferença entre a hora UTC e a hora local.</span><span class="sxs-lookup"><span data-stu-id="abda4-118">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="abda4-119">Para calcular a tendência de seu fuso horário, multiplique o número de horas em que o fuso horário está adiantado ou atrasado no horário de Greenwich (GMT) por 60 (use um número positivo para o número de horas se o fuso horário estiver à frente do GMT e um número negativo se o fuso horário estiver atrás do GMT).</span><span class="sxs-lookup"><span data-stu-id="abda4-119">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="abda4-120">Adicione um 60 adicional ao seu cálculo se o seu fuso horário estiver usando o horário de verão.</span><span class="sxs-lookup"><span data-stu-id="abda4-120">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="abda4-121">Por exemplo, o fuso horário padrão do Pacífico é de oito horas atrás do GMT, portanto, a tendência é igual a-420 (-8 \* 60 + 60) quando o horário de verão está em uso e-480 (-8 \* 60) quando o horário de verão não está em uso.</span><span class="sxs-lookup"><span data-stu-id="abda4-121">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="abda4-122">Você também pode determinar o valor da tendência consultando a propriedade Bias da classe TimeZone do [**Win32 \_**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="abda4-122">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-123">*RunRepeatedly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="abda4-123">*RunRepeatedly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="abda4-124">Se **for true**, um trabalho agendado será executado repetidamente em dias específicos.</span><span class="sxs-lookup"><span data-stu-id="abda4-124">If **True**, a scheduled job runs repeatedly on specific days.</span></span> <span data-ttu-id="abda4-125">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="abda4-125">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-126">*DaysOfWeek* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="abda4-126">*DaysOfWeek* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="abda4-127">Dias da semana em que um trabalho está agendado para ser executado; usado somente quando o parâmetro *RunRepeatedly* é **true**.</span><span class="sxs-lookup"><span data-stu-id="abda4-127">Days of the week when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span> <span data-ttu-id="abda4-128">Para agendar um trabalho para mais de um dia da semana, ingresse os valores apropriados em um OR lógico.</span><span class="sxs-lookup"><span data-stu-id="abda4-128">To schedule a job for more than one day of the week, join the appropriate values in a logical OR.</span></span> <span data-ttu-id="abda4-129">Por exemplo, para agendar um trabalho para terças e sextas-feiras, o valor de *DaysOfWeek* é 2 ou 16.</span><span class="sxs-lookup"><span data-stu-id="abda4-129">For example, to schedule a job for Tuesdays and Fridays, the value of *DaysOfWeek* are 2 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="abda4-130">**Segunda** (1)</span><span class="sxs-lookup"><span data-stu-id="abda4-130">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="abda4-131">**Terça-feira** (2)</span><span class="sxs-lookup"><span data-stu-id="abda4-131">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="abda4-132">**Quarta-feira** (4)</span><span class="sxs-lookup"><span data-stu-id="abda4-132">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="abda4-133">**Quinta-feira** (8)</span><span class="sxs-lookup"><span data-stu-id="abda4-133">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="abda4-134">**Sexta-feira** (16)</span><span class="sxs-lookup"><span data-stu-id="abda4-134">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="abda4-135">**Sábado** (32)</span><span class="sxs-lookup"><span data-stu-id="abda4-135">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="abda4-136">**Domingo** (64)</span><span class="sxs-lookup"><span data-stu-id="abda4-136">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="abda4-137">*DaysOfMonth* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="abda4-137">*DaysOfMonth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="abda4-138">Dias do mês em que um trabalho está agendado para ser executado; usado somente quando o parâmetro *RunRepeatedly* é **true**.</span><span class="sxs-lookup"><span data-stu-id="abda4-138">Days of the month when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="abda4-139"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="abda4-139"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-140">Dia 1 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-140">Day 1 of a month</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="abda4-141"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="abda4-141"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-142">Dia 2 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-142">Day 2 of a month</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="abda4-143"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="abda4-143"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-144">Dia 3 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-144">Day 3 of a month</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="abda4-145"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="abda4-145"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-146">Dia 4 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-146">Day 4 of a month</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="abda4-147"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="abda4-147"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-148">Dia 5 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-148">Day 5 of a month</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="abda4-149"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="abda4-149"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-150">Dia 6 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-150">Day 6 of a month</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="abda4-151"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="abda4-151"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-152">Dia 7 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-152">Day 7 of a month</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="abda4-153"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="abda4-153"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-154">Dia 8 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-154">Day 8 of a month</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="abda4-155"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="abda4-155"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-156">Dia 9 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-156">Day 9 of a month</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="abda4-157"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="abda4-157"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-158">Dia 10 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-158">Day 10 of a month</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="abda4-159"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="abda4-159"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-160">Dia 11 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-160">Day 11 of a month</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="abda4-161"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="abda4-161"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-162">Dia 12 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-162">Day 12 of a month</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="abda4-163"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="abda4-163"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-164">Dia 13 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-164">Day 13 of a month</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="abda4-165"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="abda4-165"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-166">Dia 14 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-166">Day 14 of a month</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="abda4-167"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="abda4-167"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-168">Dia 15 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-168">Day 15 of a month</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="abda4-169"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="abda4-169"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-170">Dia 16 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-170">Day 16 of a month</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="abda4-171"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="abda4-171"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-172">Dia 17 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-172">Day 17 of a month</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="abda4-173"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="abda4-173"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-174">Dia 18 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-174">Day 18 of a month</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="abda4-175"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="abda4-175"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-176">Dia 19 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-176">Day 19 of a month</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="abda4-177"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="abda4-177"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-178">Dia 20 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-178">Day 20 of a month</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="abda4-179"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="abda4-179"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-180">Dia 21 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-180">Day 21 of a month</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="abda4-181"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="abda4-181"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-182">Dia 22 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-182">Day 22 of a month</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="abda4-183"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="abda4-183"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-184">Dia 23 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-184">Day 23 of a month</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="abda4-185"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="abda4-185"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-186">Dia 24 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-186">Day 24 of a month</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="abda4-187"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="abda4-187"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-188">Dia 25 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-188">Day 25 of a month</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="abda4-189"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="abda4-189"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-190">Dia 26 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-190">Day 26 of a month</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="abda4-191"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="abda4-191"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-192">Dia 27 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-192">Day 27 of a month</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="abda4-193"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="abda4-193"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-194">Dia 28 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-194">Day 28 of a month</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="abda4-195"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="abda4-195"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-196">Dia 29 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-196">Day 29 of a month</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="abda4-197"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="abda4-197"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-198">Dia 30 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-198">Day 30 of a month</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="abda4-199"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="abda4-199"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="abda4-200">Dia 31 de um mês</span><span class="sxs-lookup"><span data-stu-id="abda4-200">Day 31 of a month</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="abda4-201">*InteractWithDesktop* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="abda4-201">*InteractWithDesktop* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="abda4-202">Se **for true**, o trabalho especificado deverá ser interativo, o que significa que um usuário pode fornecer entrada para um trabalho agendado enquanto o trabalho está em execução.</span><span class="sxs-lookup"><span data-stu-id="abda4-202">If **True**, the specified job should be interactive, which means that a user can give input to a scheduled job while the job is executing.</span></span> <span data-ttu-id="abda4-203">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="abda4-203">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-204">*JobID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abda4-204">*JobId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abda4-205">Número de identificador de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="abda4-205">Identifier number of a job.</span></span> <span data-ttu-id="abda4-206">Esse parâmetro é um identificador para um trabalho que está sendo agendado em um computador.</span><span class="sxs-lookup"><span data-stu-id="abda4-206">This parameter is a handle to a job being scheduled on a computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abda4-207">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abda4-207">Return value</span></span>

<span data-ttu-id="abda4-208">Retorna um valor de 0 (zero) quando bem-sucedido e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="abda4-208">Returns a value of 0 (zero) when successful, and a different number to indicate an error.</span></span> <span data-ttu-id="abda4-209">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="abda4-209">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="abda4-210">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="abda4-210">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="abda4-211">**Conclusão bem-sucedida**</span><span class="sxs-lookup"><span data-stu-id="abda4-211">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="abda4-212">0</span><span class="sxs-lookup"><span data-stu-id="abda4-212">0</span></span>

<span data-ttu-id="abda4-213">A solicitação é aceita.</span><span class="sxs-lookup"><span data-stu-id="abda4-213">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-214">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="abda4-214">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="abda4-215">1</span><span class="sxs-lookup"><span data-stu-id="abda4-215">1</span></span>

<span data-ttu-id="abda4-216">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="abda4-216">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-217">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="abda4-217">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="abda4-218">2</span><span class="sxs-lookup"><span data-stu-id="abda4-218">2</span></span>

<span data-ttu-id="abda4-219">O usuário não tem o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="abda4-219">The user does not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-220">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="abda4-220">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="abda4-221">8</span><span class="sxs-lookup"><span data-stu-id="abda4-221">8</span></span>

<span data-ttu-id="abda4-222">Processo interativo.</span><span class="sxs-lookup"><span data-stu-id="abda4-222">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-223">**demarcador não localizado**</span><span class="sxs-lookup"><span data-stu-id="abda4-223">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="abda4-224">9</span><span class="sxs-lookup"><span data-stu-id="abda4-224">9</span></span>

<span data-ttu-id="abda4-225">Não é possível encontrar o caminho do diretório para o arquivo executável do serviço.</span><span class="sxs-lookup"><span data-stu-id="abda4-225">The directory path to the service executable file cannot be found.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-226">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="abda4-226">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="abda4-227">21</span><span class="sxs-lookup"><span data-stu-id="abda4-227">21</span></span>

<span data-ttu-id="abda4-228">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="abda4-228">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-229">**Serviço não iniciado**</span><span class="sxs-lookup"><span data-stu-id="abda4-229">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="abda4-230">22</span><span class="sxs-lookup"><span data-stu-id="abda4-230">22</span></span>

<span data-ttu-id="abda4-231">A conta em que esse serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="abda4-231">The account that this service runs under is invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="abda4-232">**Outras**</span><span class="sxs-lookup"><span data-stu-id="abda4-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="abda4-233">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="abda4-233">23 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abda4-234">Comentários</span><span class="sxs-lookup"><span data-stu-id="abda4-234">Remarks</span></span>

<span data-ttu-id="abda4-235">Se o trabalho agendado iniciar um programa interativo, como o bloco de notas, a propriedade **InteractWithDeskto** deverá ser definida como **true** ou a tela do programa não ficará visível.</span><span class="sxs-lookup"><span data-stu-id="abda4-235">If your scheduled job starts an interactive program such as Notepad, then the **InteractWithDeskto** property must be set to **True** or the program's screen is not visible.</span></span> <span data-ttu-id="abda4-236">O processo ainda aparece no **Gerenciador de tarefas** , mesmo que ele não apareça na tela.</span><span class="sxs-lookup"><span data-stu-id="abda4-236">The process still appears in the **Task Manager** even if it does not appear on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="abda4-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abda4-237">Requirements</span></span>



| <span data-ttu-id="abda4-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="abda4-238">Requirement</span></span> | <span data-ttu-id="abda4-239">Valor</span><span class="sxs-lookup"><span data-stu-id="abda4-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abda4-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abda4-240">Minimum supported client</span></span><br/> | <span data-ttu-id="abda4-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abda4-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abda4-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abda4-242">Minimum supported server</span></span><br/> | <span data-ttu-id="abda4-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abda4-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abda4-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="abda4-244">Namespace</span></span><br/>                | <span data-ttu-id="abda4-245">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="abda4-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="abda4-246">MOF</span><span class="sxs-lookup"><span data-stu-id="abda4-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abda4-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abda4-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="abda4-248">DLL</span><span class="sxs-lookup"><span data-stu-id="abda4-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abda4-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abda4-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abda4-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="abda4-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="abda4-251">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="abda4-251">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="abda4-252">**\_ScheduledJob Win32**</span><span class="sxs-lookup"><span data-stu-id="abda4-252">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

