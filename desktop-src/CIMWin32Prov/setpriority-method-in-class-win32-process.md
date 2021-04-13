---
description: A&de desanterioridade \# 32; O método de classe WMI tenta alterar a prioridade de execução do processo.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Método setanteriority da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501073"
---
# <a name="setpriority-method-of-the-win32_process-class"></a><span data-ttu-id="11717-103">Método setanteriority da \_ classe Process do Win32</span><span class="sxs-lookup"><span data-stu-id="11717-103">SetPriority method of the Win32\_Process class</span></span>

<span data-ttu-id="11717-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **setanteriority** tenta alterar a prioridade de execução do processo.</span><span class="sxs-lookup"><span data-stu-id="11717-104">The **SetPriority** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to change the execution priority of the process.</span></span>

<span data-ttu-id="11717-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="11717-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="11717-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="11717-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="11717-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11717-107">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="11717-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11717-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11717-109">*Prioridade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="11717-109">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11717-110">Nova classe de prioridade para o processo.</span><span class="sxs-lookup"><span data-stu-id="11717-110">New priority class for the process.</span></span> <span data-ttu-id="11717-111">Observe que esses valores são diferentes daqueles explicitamente indicados na propriedade **Priority** do [**\_ processo Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="11717-111">Note that these values are different than those explicitly stated in the **Priority** property of [**Win32\_Process**](win32-process.md).</span></span>

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="11717-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Ocioso** (64)</span><span class="sxs-lookup"><span data-stu-id="11717-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="11717-113">Especificado para um processo com threads que são executados somente quando o sistema está ocioso.</span><span class="sxs-lookup"><span data-stu-id="11717-113">Specified for a process with threads that run only when the system is idle.</span></span> <span data-ttu-id="11717-114">Os threads do processo são admitidos pelos threads de um processo executado em uma classe de prioridade mais alta, por exemplo, uma proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="11717-114">The threads of the process are preempted by the threads of a process that run in a higher priority class, for example, a screen saver.</span></span> <span data-ttu-id="11717-115">A classe de prioridade ociosa é herdada por processos filho.</span><span class="sxs-lookup"><span data-stu-id="11717-115">The idle-priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="11717-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Abaixo do normal** (16384)</span><span class="sxs-lookup"><span data-stu-id="11717-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="11717-117">Indica um processo que tem prioridade acima **da \_ \_ classe de prioridade ociosa**, mas abaixo da **\_ \_ classe de prioridade normal**.</span><span class="sxs-lookup"><span data-stu-id="11717-117">Indicates a process that has priority above **IDLE\_PRIORITY\_CLASS**, but below **NORMAL\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="11717-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="11717-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="11717-119">Especificado para um processo sem necessidade de agendamento especial.</span><span class="sxs-lookup"><span data-stu-id="11717-119">Specified for a process with no special scheduling needs.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="11717-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Acima do normal** (32768)</span><span class="sxs-lookup"><span data-stu-id="11717-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="11717-121">Indica um processo que tem prioridade acima **da \_ \_ classe de prioridade normal**, mas abaixo da **\_ \_ classe de prioridade alta**.</span><span class="sxs-lookup"><span data-stu-id="11717-121">Indicates a process that has priority above **NORMAL\_PRIORITY\_CLASS**, but below **HIGH\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span data-ttu-id="11717-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Alta prioridade** (128)</span><span class="sxs-lookup"><span data-stu-id="11717-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**High Priority** (128)</span></span>


</dt> <dd>

<span data-ttu-id="11717-123">Especificado para um processo que executa tarefas de tempo crítico que devem ser executadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="11717-123">Specified for a process that performs time-critical tasks that must be executed immediately.</span></span> <span data-ttu-id="11717-124">Os threads do processo capturam os threads de processos da classe de prioridade normal ou ociosa.</span><span class="sxs-lookup"><span data-stu-id="11717-124">The threads of the process preempt the threads of normal or idle priority class processes.</span></span> <span data-ttu-id="11717-125">Um exemplo é o Lista de Tarefas, que deve responder rapidamente quando chamado pelo usuário, independentemente da carga no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="11717-125">An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="11717-126">Use extrema atenção ao usar a classe de alta prioridade, porque um aplicativo de classe de alta prioridade pode usar quase todo o tempo de CPU disponível.</span><span class="sxs-lookup"><span data-stu-id="11717-126">Use extreme care when using the high-priority class, because a high-priority class application can use nearly all of the available CPU time.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="11717-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo real** (256)</span><span class="sxs-lookup"><span data-stu-id="11717-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="11717-128">Especificado para um processo que tem a maior prioridade possível.</span><span class="sxs-lookup"><span data-stu-id="11717-128">Specified for a process that has the highest possible priority.</span></span> <span data-ttu-id="11717-129">Os threads do processo antecipam os threads de todos os outros processos, incluindo processos do sistema operacional que executam tarefas importantes.</span><span class="sxs-lookup"><span data-stu-id="11717-129">The threads of the process preempt the threads of all of the other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="11717-130">Por exemplo, um processo em tempo real que é executado por mais de um intervalo muito curto pode fazer com que os caches de disco não sejam liberados ou um mouse não responda.</span><span class="sxs-lookup"><span data-stu-id="11717-130">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or a mouse to be unresponsive.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11717-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11717-131">Return value</span></span>

<span data-ttu-id="11717-132">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="11717-132">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="11717-133">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="11717-133">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="11717-134">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="11717-134">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="11717-135">**Conclusão bem-sucedida** (0)</span><span class="sxs-lookup"><span data-stu-id="11717-135">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="11717-136">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="11717-136">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="11717-137">**Privilégio insuficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="11717-137">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="11717-138">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="11717-138">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="11717-139">**Caminho não encontrado** (9)</span><span class="sxs-lookup"><span data-stu-id="11717-139">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="11717-140">**Parâmetro inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="11717-140">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="11717-141">**Outro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="11717-141">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="11717-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="11717-142">Remarks</span></span>

<span data-ttu-id="11717-143">Para definir a prioridade em tempo real, o chamador deve ter o **SeIncreaseBasePriorityPrivilege** (**\_ \_ \_ \_ privilégio de prioridade base do se Inc**).</span><span class="sxs-lookup"><span data-stu-id="11717-143">To set the priority to Realtime, the caller must have **SeIncreaseBasePriorityPrivilege** (**SE\_INC\_BASE\_PRIORITY\_PRIVILEGE**).</span></span> <span data-ttu-id="11717-144">Sem esse privilégio, a prioridade mais alta pode ser definida como prioridade alta.</span><span class="sxs-lookup"><span data-stu-id="11717-144">Without this privilege, the highest the priority can be set to is High Priority.</span></span>

## <a name="examples"></a><span data-ttu-id="11717-145">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11717-145">Examples</span></span>

<span data-ttu-id="11717-146">A amostra [Modificar a prioridade de um processo em execução](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) do VBScript altera a prioridade de uma instância em execução do Notepad.exe de normal para acima normal.</span><span class="sxs-lookup"><span data-stu-id="11717-146">The [Modify the Priority Of a Running Process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript sample changes the priority of a running instance of Notepad.exe from Normal to Above Normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="11717-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11717-147">Requirements</span></span>



| <span data-ttu-id="11717-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="11717-148">Requirement</span></span> | <span data-ttu-id="11717-149">Valor</span><span class="sxs-lookup"><span data-stu-id="11717-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11717-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11717-150">Minimum supported client</span></span><br/> | <span data-ttu-id="11717-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11717-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11717-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11717-152">Minimum supported server</span></span><br/> | <span data-ttu-id="11717-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11717-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11717-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="11717-154">Namespace</span></span><br/>                | <span data-ttu-id="11717-155">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="11717-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="11717-156">MOF</span><span class="sxs-lookup"><span data-stu-id="11717-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11717-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11717-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="11717-158">DLL</span><span class="sxs-lookup"><span data-stu-id="11717-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11717-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11717-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11717-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="11717-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="11717-161">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11717-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="11717-162">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="11717-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

