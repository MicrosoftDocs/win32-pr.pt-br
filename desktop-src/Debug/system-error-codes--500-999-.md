---
description: Descreve os códigos de erro 500-999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Códigos de erro do sistema (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164102"
---
# <a name="system-error-codes-500-999"></a><span data-ttu-id="69e9e-103">Códigos de erro do sistema (500-999)</span><span class="sxs-lookup"><span data-stu-id="69e9e-103">System Error Codes (500-999)</span></span>

> [!NOTE]
> <span data-ttu-id="69e9e-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="69e9e-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="69e9e-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="69e9e-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 500 a 999).</span><span class="sxs-lookup"><span data-stu-id="69e9e-106">The following list describes [system error codes](system-error-codes.md) (errors 500 to 999).</span></span> <span data-ttu-id="69e9e-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="69e9e-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="69e9e-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="69e9e-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="69e9e-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERRO \_ ao \_ carregar perfil do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR\_USER\_PROFILE\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-110">500 (0x1F4)</span><span class="sxs-lookup"><span data-stu-id="69e9e-110">500 (0x1F4)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-111">Não é possível carregar o perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="69e9e-111">User profile cannot be loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**\_estouro aritmético de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERROR\_ARITHMETIC\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-113">534 (0x216)</span><span class="sxs-lookup"><span data-stu-id="69e9e-113">534 (0x216)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-114">O resultado aritmético excedeu 32 bits.</span><span class="sxs-lookup"><span data-stu-id="69e9e-114">Arithmetic result exceeded 32 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**PIPE de erro \_ \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**ERROR\_PIPE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-116">535 (0x217)</span><span class="sxs-lookup"><span data-stu-id="69e9e-116">535 (0x217)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-117">Há um processo em outra extremidade do pipe.</span><span class="sxs-lookup"><span data-stu-id="69e9e-117">There is a process on other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**\_escuta de pipe de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**ERROR\_PIPE\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-119">536 (0x218)</span><span class="sxs-lookup"><span data-stu-id="69e9e-119">536 (0x218)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-120">Aguardando um processo abrir a outra extremidade do pipe.</span><span class="sxs-lookup"><span data-stu-id="69e9e-120">Waiting for a process to open the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**\_interrupção do verificador de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**ERROR\_VERIFIER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-122">537 (0x219)</span><span class="sxs-lookup"><span data-stu-id="69e9e-122">537 (0x219)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-123">O verificador de aplicativo encontrou um erro no processo atual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-123">Application verifier has found an error in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**erro \_ ABIOS \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**ERROR\_ABIOS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-125">538 (0x21A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-125">538 (0x21A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-126">Ocorreu um erro no subsistema ABIOS.</span><span class="sxs-lookup"><span data-stu-id="69e9e-126">An error occurred in the ABIOS subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**\_Aviso de WX86 de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR\_WX86\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-128">539 (0x21B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-128">539 (0x21B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-129">Ocorreu um aviso no subsistema WX86.</span><span class="sxs-lookup"><span data-stu-id="69e9e-129">A warning occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Erro \_ WX86 \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**ERROR\_WX86\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-131">540 (0x21C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-131">540 (0x21C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-132">Ocorreu um erro no subsistema WX86.</span><span class="sxs-lookup"><span data-stu-id="69e9e-132">An error occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**\_temporizador de erro \_ não \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**ERROR\_TIMER\_NOT\_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-134">541 (0x21D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-134">541 (0x21D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-135">Foi feita uma tentativa de cancelar ou definir um temporizador que tem uma APC associada e o thread do assunto não é o thread que originalmente definiu o temporizador com uma rotina APC associada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-135">An attempt was made to cancel or set a timer that has an associated APC and the subject thread is not the thread that originally set the timer with an associated APC routine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**\_desenrolar erro**</span><span class="sxs-lookup"><span data-stu-id="69e9e-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR\_UNWIND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-137">542 (0x21E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-137">542 (0x21E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-138">Desenrolar código de exceção.</span><span class="sxs-lookup"><span data-stu-id="69e9e-138">Unwind exception code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERRO \_ de \_ pilha inadequada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR\_BAD\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-140">543 (0x21F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-140">543 (0x21F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-141">Uma pilha inválida ou não alinhada foi encontrada durante uma operação de desenrolamento.</span><span class="sxs-lookup"><span data-stu-id="69e9e-141">An invalid or unaligned stack was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**\_destino de \_ liberação \_ inválido de erro**</span><span class="sxs-lookup"><span data-stu-id="69e9e-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR\_INVALID\_UNWIND\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-143">544 (0x220)</span><span class="sxs-lookup"><span data-stu-id="69e9e-143">544 (0x220)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-144">Um destino de desenrolamento inválido foi encontrado durante uma operação de desenrolamento.</span><span class="sxs-lookup"><span data-stu-id="69e9e-144">An invalid unwind target was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERRO \_ de \_ atributos de porta inválidos \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR\_INVALID\_PORT\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-146">545 (0x221)</span><span class="sxs-lookup"><span data-stu-id="69e9e-146">545 (0x221)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-147">Atributos de objeto inválidos especificados para NtCreatePort ou atributos de porta inválidos especificados para NtConnectPort</span><span class="sxs-lookup"><span data-stu-id="69e9e-147">Invalid Object Attributes specified to NtCreatePort or invalid Port Attributes specified to NtConnectPort</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**mensagem de porta de erro \_ \_ \_ muito \_ longa**</span><span class="sxs-lookup"><span data-stu-id="69e9e-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**ERROR\_PORT\_MESSAGE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-149">546 (0x222)</span><span class="sxs-lookup"><span data-stu-id="69e9e-149">546 (0x222)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-150">O comprimento da mensagem passado para NtRequestPort ou NtRequestWaitReplyPort foi maior do que a mensagem máxima permitida pela porta.</span><span class="sxs-lookup"><span data-stu-id="69e9e-150">Length of message passed to NtRequestPort or NtRequestWaitReplyPort was longer than the maximum message allowed by the port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERRO \_ de \_ cota inválida \_ inferior**</span><span class="sxs-lookup"><span data-stu-id="69e9e-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR\_INVALID\_QUOTA\_LOWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-152">547 (0x223)</span><span class="sxs-lookup"><span data-stu-id="69e9e-152">547 (0x223)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-153">Foi feita uma tentativa de reduzir um limite de cota abaixo do uso atual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-153">An attempt was made to lower a quota limit below the current usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**dispositivo de erro \_ \_ já \_ anexado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**ERROR\_DEVICE\_ALREADY\_ATTACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-155">548 (0x224)</span><span class="sxs-lookup"><span data-stu-id="69e9e-155">548 (0x224)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-156">Foi feita uma tentativa de anexar a um dispositivo que já estava anexado a outro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-156">An attempt was made to attach to a device that was already attached to another device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**inalinhamento de instrução de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR\_INSTRUCTION\_MISALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-158">549 (0x225)</span><span class="sxs-lookup"><span data-stu-id="69e9e-158">549 (0x225)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-159">Foi feita uma tentativa de executar uma instrução em um endereço não alinhado e o sistema host não oferece suporte a referências de instruções não alinhadas.</span><span class="sxs-lookup"><span data-stu-id="69e9e-159">An attempt was made to execute an instruction at an unaligned address and the host system does not support unaligned instruction references.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**criação de perfil de erro \_ \_ não \_ iniciada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR\_PROFILING\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-161">550 (0x226)</span><span class="sxs-lookup"><span data-stu-id="69e9e-161">550 (0x226)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-162">A criação de perfil não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-162">Profiling not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**criação de perfil de erro \_ \_ não \_ parada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERROR\_PROFILING\_NOT\_STOPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-164">551 (0x227)</span><span class="sxs-lookup"><span data-stu-id="69e9e-164">551 (0x227)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-165">A criação de perfil não foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-165">Profiling not stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERRO \_ não foi possível \_ \_ interpretar**</span><span class="sxs-lookup"><span data-stu-id="69e9e-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR\_COULD\_NOT\_INTERPRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-167">552 (0x228)</span><span class="sxs-lookup"><span data-stu-id="69e9e-167">552 (0x228)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-168">A ACL passada não continha as informações mínimas necessárias.</span><span class="sxs-lookup"><span data-stu-id="69e9e-168">The passed ACL did not contain the minimum required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**\_criação de perfil \_ de erro em \_ limite**</span><span class="sxs-lookup"><span data-stu-id="69e9e-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR\_PROFILING\_AT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-170">553 (0x229)</span><span class="sxs-lookup"><span data-stu-id="69e9e-170">553 (0x229)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-171">O número de objetos de criação de perfil ativos está no máximo e não é mais possível iniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-171">The number of active profiling objects is at the maximum and no more may be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERRO não é possível \_ \_ aguardar**</span><span class="sxs-lookup"><span data-stu-id="69e9e-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR\_CANT\_WAIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-173">554 (0x22A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-173">554 (0x22A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-174">Usado para indicar que uma operação não pode continuar sem bloqueio de e/s.</span><span class="sxs-lookup"><span data-stu-id="69e9e-174">Used to indicate that an operation cannot continue without blocking for I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERRO não é possível \_ \_ encerrar \_ automaticamente**</span><span class="sxs-lookup"><span data-stu-id="69e9e-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR\_CANT\_TERMINATE\_SELF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-176">555 (0x22B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-176">555 (0x22B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-177">Indica que um thread tentou se encerrar por padrão (chamado NtTerminateThread com **NULL**) e foi o último thread no processo atual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-177">Indicates that a thread attempted to terminate itself by default (called NtTerminateThread with **NULL**) and it was the last thread in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERRO \_ inesperado ao \_ criar erro mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR\_UNEXPECTED\_MM\_CREATE\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-179">556 (0x22C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-179">556 (0x22C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-180">Se um erro MM for retornado, o que não está definido no filtro FsRtl padrão, ele será convertido em um dos seguintes erros que tem a garantia de estar no filtro.</span><span class="sxs-lookup"><span data-stu-id="69e9e-180">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="69e9e-181">No entanto, nesse caso, as informações são perdidas, mas o filtro manipula corretamente a exceção.</span><span class="sxs-lookup"><span data-stu-id="69e9e-181">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**erro erro de \_ \_ \_ mapeamento \_ mm inesperado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**ERROR\_UNEXPECTED\_MM\_MAP\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-183">557 (0x22D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-183">557 (0x22D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-184">Se um erro MM for retornado, o que não está definido no filtro FsRtl padrão, ele será convertido em um dos seguintes erros que tem a garantia de estar no filtro.</span><span class="sxs-lookup"><span data-stu-id="69e9e-184">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="69e9e-185">No entanto, nesse caso, as informações são perdidas, mas o filtro manipula corretamente a exceção.</span><span class="sxs-lookup"><span data-stu-id="69e9e-185">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERRO \_ inesperado ao \_ \_ estender \_ Err**</span><span class="sxs-lookup"><span data-stu-id="69e9e-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR\_UNEXPECTED\_MM\_EXTEND\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-187">558 (0x22E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-187">558 (0x22E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-188">Se um erro MM for retornado, o que não está definido no filtro FsRtl padrão, ele será convertido em um dos seguintes erros que tem a garantia de estar no filtro.</span><span class="sxs-lookup"><span data-stu-id="69e9e-188">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="69e9e-189">No entanto, nesse caso, as informações são perdidas, mas o filtro manipula corretamente a exceção.</span><span class="sxs-lookup"><span data-stu-id="69e9e-189">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERRO \_ de \_ tabela de função inadequada \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR\_BAD\_FUNCTION\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-191">559 (0x22F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-191">559 (0x22F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-192">Uma tabela de funções malformada foi encontrada durante uma operação de desenrolamento.</span><span class="sxs-lookup"><span data-stu-id="69e9e-192">A malformed function table was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERRO \_ sem \_ tradução de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR\_NO\_GUID\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-194">560 (0x230)</span><span class="sxs-lookup"><span data-stu-id="69e9e-194">560 (0x230)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-195">Indica que foi feita uma tentativa de atribuir proteção a um arquivo do sistema de arquivos ou diretório, e um dos SIDs no descritor de segurança não pôde ser convertido em um GUID que pudesse ser armazenado pelo sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-195">Indicates that an attempt was made to assign protection to a file system file or directory and one of the SIDs in the security descriptor could not be translated into a GUID that could be stored by the file system.</span></span> <span data-ttu-id="69e9e-196">Isso faz com que a tentativa de proteção falhe, o que pode causar uma falha na tentativa de criação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-196">This causes the protection attempt to fail, which may cause a file creation attempt to fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERRO \_ de \_ tamanho inválido de LDT \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR\_INVALID\_LDT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-198">561 (0x231)</span><span class="sxs-lookup"><span data-stu-id="69e9e-198">561 (0x231)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-199">Indica que foi feita uma tentativa de aumentar um LDT definindo seu tamanho ou que o tamanho não era um número par de seletores.</span><span class="sxs-lookup"><span data-stu-id="69e9e-199">Indicates that an attempt was made to grow an LDT by setting its size, or that the size was not an even number of selectors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERRO \_ de \_ deslocamento de LDT inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR\_INVALID\_LDT\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-201">563 (0x233)</span><span class="sxs-lookup"><span data-stu-id="69e9e-201">563 (0x233)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-202">Indica que o valor inicial para as informações de LDT não era um múltiplo integral do tamanho do seletor.</span><span class="sxs-lookup"><span data-stu-id="69e9e-202">Indicates that the starting value for the LDT information was not an integral multiple of the selector size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERRO \_ \_ descritor de LDT inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR\_INVALID\_LDT\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-204">564 (0x234)</span><span class="sxs-lookup"><span data-stu-id="69e9e-204">564 (0x234)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-205">Indica que o usuário forneceu um descritor inválido ao tentar configurar os descritores do LDT.</span><span class="sxs-lookup"><span data-stu-id="69e9e-205">Indicates that the user supplied an invalid descriptor when trying to set up Ldt descriptors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERRO \_ de \_ muitos \_ threads**</span><span class="sxs-lookup"><span data-stu-id="69e9e-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR\_TOO\_MANY\_THREADS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-207">565 (0x235)</span><span class="sxs-lookup"><span data-stu-id="69e9e-207">565 (0x235)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-208">Indica que um processo tem muitos threads para executar a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-208">Indicates a process has too many threads to perform the requested action.</span></span> <span data-ttu-id="69e9e-209">Por exemplo, a atribuição de um token primário só pode ser executada quando um processo tem zero ou um thread.</span><span class="sxs-lookup"><span data-stu-id="69e9e-209">For example, assignment of a primary token may only be performed when a process has zero or one threads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**\_thread \_ de erro não está \_ em \_ processo**</span><span class="sxs-lookup"><span data-stu-id="69e9e-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**ERROR\_THREAD\_NOT\_IN\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-211">566 (0x236)</span><span class="sxs-lookup"><span data-stu-id="69e9e-211">566 (0x236)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-212">Foi feita uma tentativa de operar em um thread dentro de um processo específico, mas o thread especificado não está no processo especificado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-212">An attempt was made to operate on a thread within a specific process, but the thread specified is not in the process specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**\_cota de arquivo de paginação de erro \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="69e9e-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERROR\_PAGEFILE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-214">567 (0x237)</span><span class="sxs-lookup"><span data-stu-id="69e9e-214">567 (0x237)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-215">A cota do arquivo de paginação foi excedida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-215">Page file quota was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**\_ \_ conflito do servidor de logon de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERROR\_LOGON\_SERVER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-217">568 (0x238)</span><span class="sxs-lookup"><span data-stu-id="69e9e-217">568 (0x238)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-218">O serviço Netlogon não pode ser iniciado porque outro serviço Netlogon em execução no domínio está em conflito com a função especificada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-218">The Netlogon service cannot start because another Netlogon service running in the domain conflicts with the specified role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**sincronização de erro \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="69e9e-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**ERROR\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-220">569 (0x239)</span><span class="sxs-lookup"><span data-stu-id="69e9e-220">569 (0x239)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-221">O banco de dados SAM em um Windows Server é significativamente fora de sincronização com a cópia no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="69e9e-221">The SAM database on a Windows Server is significantly out of synchronization with the copy on the Domain Controller.</span></span> <span data-ttu-id="69e9e-222">Uma sincronização completa é necessária.</span><span class="sxs-lookup"><span data-stu-id="69e9e-222">A complete synchronization is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERRO \_ net \_ Open \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="69e9e-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR\_NET\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-224">570 (0x23A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-224">570 (0x23A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-225">Falha na API NtCreateFile.</span><span class="sxs-lookup"><span data-stu-id="69e9e-225">The NtCreateFile API failed.</span></span> <span data-ttu-id="69e9e-226">Esse erro nunca deve ser retornado a um aplicativo, é um espaço reservado para o redirecionador do Gerenciador de LAN do Windows usar em suas rotinas de mapeamento de erros internas.</span><span class="sxs-lookup"><span data-stu-id="69e9e-226">This error should never be returned to an application, it is a place holder for the Windows Lan Manager Redirector to use in its internal error mapping routines.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**\_ \_ falha no privilégio de es de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR\_IO\_PRIVILEGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-228">571 (0x23B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-228">571 (0x23B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-229">{Falha no privilégio} Não foi possível alterar as permissões de e/s do processo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-229">{Privilege Failed} The I/O permissions for the process could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**sair do controle de erro \_ \_ C \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR\_CONTROL\_C\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-231">572 (0x23C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-231">572 (0x23C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-232">{Saída do aplicativo por CTRL + C} O aplicativo foi encerrado como resultado de um CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="69e9e-232">{Application Exit by CTRL+C} The application terminated as a result of a CTRL+C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERRO \_ de \_ systemfile ausente**</span><span class="sxs-lookup"><span data-stu-id="69e9e-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR\_MISSING\_SYSTEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-234">573 (0x23D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-234">573 (0x23D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-235">{Arquivo de sistema ausente} O arquivo de sistema necessário% HS está insatisfatório ou ausente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-235">{Missing System File} The required system file %hs is bad or missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERRO de \_ exceção sem tratamento \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR\_UNHANDLED\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-237">574 (0x23E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-237">574 (0x23E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-238">{Erro de aplicativo} A exceção% s (0x% 08lx) ocorreu no aplicativo no local 0x% 08lx.</span><span class="sxs-lookup"><span data-stu-id="69e9e-238">{Application Error} The exception %s (0x%08lx) occurred in the application at location 0x%08lx.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**\_ \_ falha na inicialização do aplicativo de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR\_APP\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-240">575 (0x23F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-240">575 (0x23F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-241">{Erro de aplicativo} O aplicativo não pôde ser iniciado corretamente (0x% lx).</span><span class="sxs-lookup"><span data-stu-id="69e9e-241">{Application Error} The application was unable to start correctly (0x%lx).</span></span> <span data-ttu-id="69e9e-242">Clique em OK para fechar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-242">Click OK to close the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERRO \_ \_ ao criar arquivo de paginação \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR\_PAGEFILE\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-244">576 (0x240)</span><span class="sxs-lookup"><span data-stu-id="69e9e-244">576 (0x240)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-245">{Não é possível criar arquivo de paginação} Falha na criação do arquivo de paginação% HS (% LX).</span><span class="sxs-lookup"><span data-stu-id="69e9e-245">{Unable to Create Paging File} The creation of the paging file %hs failed (%lx).</span></span> <span data-ttu-id="69e9e-246">O tamanho solicitado era% ld.</span><span class="sxs-lookup"><span data-stu-id="69e9e-246">The requested size was %ld.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERRO \_ de \_ hash de imagem inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR\_INVALID\_IMAGE\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-248">577 (0x241)</span><span class="sxs-lookup"><span data-stu-id="69e9e-248">577 (0x241)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-249">O Windows não pode verificar a assinatura digital deste arquivo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-249">Windows cannot verify the digital signature for this file.</span></span> <span data-ttu-id="69e9e-250">Uma alteração recente de hardware ou software pode ter instalado um arquivo que está assinado incorretamente ou danificado ou que pode ser um software mal-intencionado de uma fonte desconhecida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-250">A recent hardware or software change might have installed a file that is signed incorrectly or damaged, or that might be malicious software from an unknown source.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERRO \_ sem \_ arquivo de paginação**</span><span class="sxs-lookup"><span data-stu-id="69e9e-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR\_NO\_PAGEFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-252">578 (0x242)</span><span class="sxs-lookup"><span data-stu-id="69e9e-252">578 (0x242)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-253">{Nenhum arquivo de paginação especificado} Nenhum arquivo de paginação foi especificado na configuração do sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-253">{No Paging File Specified} No paging file was specified in the system configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERRO \_ de \_ contexto flutuante inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR\_ILLEGAL\_FLOAT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-255">579 (0x243)</span><span class="sxs-lookup"><span data-stu-id="69e9e-255">579 (0x243)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-256">Exception Um aplicativo de modo real emitiu uma instrução de ponto flutuante e um hardware de ponto flutuante não está presente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-256">{EXCEPTION} A real-mode application issued a floating-point instruction and floating-point hardware is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERRO \_ nenhum \_ par de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERROR\_NO\_EVENT\_PAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-258">580 (0x244)</span><span class="sxs-lookup"><span data-stu-id="69e9e-258">580 (0x244)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-259">Uma operação de sincronização de par de eventos foi executada usando o objeto de par de eventos de cliente/servidor específico do thread, mas nenhum objeto de par de eventos foi associado ao thread.</span><span class="sxs-lookup"><span data-stu-id="69e9e-259">An event pair synchronization operation was performed using the thread specific client/server event pair object, but no event pair object was associated with the thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**erro \_ de \_ configuração do CTRL do domínio de \_ erros \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**ERROR\_DOMAIN\_CTRLR\_CONFIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-261">581 (0x245)</span><span class="sxs-lookup"><span data-stu-id="69e9e-261">581 (0x245)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-262">Um Windows Server tem uma configuração incorreta.</span><span class="sxs-lookup"><span data-stu-id="69e9e-262">A Windows Server has an incorrect configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**\_caractere inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR\_ILLEGAL\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-264">582 (0x246)</span><span class="sxs-lookup"><span data-stu-id="69e9e-264">582 (0x246)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-265">Um caractere inválido foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-265">An illegal character was encountered.</span></span> <span data-ttu-id="69e9e-266">Para um conjunto de caracteres de vários bytes, isso inclui um byte de Lead sem um byte de trilha com sucesso.</span><span class="sxs-lookup"><span data-stu-id="69e9e-266">For a multi-byte character set this includes a lead byte without a succeeding trail byte.</span></span> <span data-ttu-id="69e9e-267">Para o conjunto de caracteres Unicode, isso inclui os caracteres 0xFFFF e 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="69e9e-267">For the Unicode character set this includes the characters 0xFFFF and 0xFFFE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERRO de \_ caractere INdefinido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERROR\_UNDEFINED\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-269">583 (0x247)</span><span class="sxs-lookup"><span data-stu-id="69e9e-269">583 (0x247)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-270">O caractere Unicode não está definido no conjunto de caracteres Unicode instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-270">The Unicode character is not defined in the Unicode character set installed on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERRO \_ de \_ volume de disquete**</span><span class="sxs-lookup"><span data-stu-id="69e9e-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERROR\_FLOPPY\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-272">584 (0x248)</span><span class="sxs-lookup"><span data-stu-id="69e9e-272">584 (0x248)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-273">O arquivo de paginação não pode ser criado em um disquete.</span><span class="sxs-lookup"><span data-stu-id="69e9e-273">The paging file cannot be created on a floppy diskette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERRO o \_ BIOS \_ falhou ao \_ \_ conectar a \_ interrupção**</span><span class="sxs-lookup"><span data-stu-id="69e9e-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR\_BIOS\_FAILED\_TO\_CONNECT\_INTERRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-275">585 (0x249)</span><span class="sxs-lookup"><span data-stu-id="69e9e-275">585 (0x249)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-276">O BIOS do sistema falhou ao conectar uma interrupção do sistema ao dispositivo ou ao barramento para o qual o dispositivo está conectado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-276">The system BIOS failed to connect a system interrupt to the device or bus for which the device is connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERRO \_ no \_ controlador de backup**</span><span class="sxs-lookup"><span data-stu-id="69e9e-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR\_BACKUP\_CONTROLLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-278">586 (0x24A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-278">586 (0x24A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-279">Esta operação só é permitida para o controlador de domínio primário do domínio.</span><span class="sxs-lookup"><span data-stu-id="69e9e-279">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**limite de Mutant de erro \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="69e9e-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERROR\_MUTANT\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-281">587 (0x24B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-281">587 (0x24B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-282">Foi feita uma tentativa de adquirir um Mutant de modo que sua contagem máxima teria sido excedida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-282">An attempt was made to acquire a mutant such that its maximum count would have been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**Driver de erro \_ FS \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="69e9e-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR\_FS\_DRIVER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-284">588 (0x24C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-284">588 (0x24C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-285">Um volume foi acessado para o qual um driver de sistema de arquivos é necessário e ainda não foi carregado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-285">A volume has been accessed for which a file system driver is required that has not yet been loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERRO \_ não é possível \_ carregar o \_ arquivo do registro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR\_CANNOT\_LOAD\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-287">589 (0x24D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-287">589 (0x24D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-288">{Falha no arquivo do registro} O registro não pode carregar o hive (arquivo):% HS ou seu log ou alternativo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-288">{Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate.</span></span> <span data-ttu-id="69e9e-289">Ele está corrompido, ausente ou não é gravável.</span><span class="sxs-lookup"><span data-stu-id="69e9e-289">It is corrupt, absent, or not writable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERRO \_ \_ ao anexar a depuração \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR\_DEBUG\_ATTACH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-291">590 (0x24E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-291">590 (0x24E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-292">{Falha inesperada em [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Ocorreu uma falha inesperada ao processar uma solicitação de API **DebugActiveProcess** .</span><span class="sxs-lookup"><span data-stu-id="69e9e-292">{Unexpected Failure in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} An unexpected failure occurred while processing a **DebugActiveProcess** API request.</span></span> <span data-ttu-id="69e9e-293">Você pode escolher OK para encerrar o processo ou cancelar para ignorar o erro.</span><span class="sxs-lookup"><span data-stu-id="69e9e-293">You may choose OK to terminate the process, or Cancel to ignore the error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**processo do sistema de erros \_ \_ \_ encerrado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR\_SYSTEM\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-295">591 (0x24F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-295">591 (0x24F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-296">{Erro fatal do sistema} O processo do sistema% HS foi finalizado inesperadamente com um status de 0x% 08x (0x% 08x 0x% 08x).</span><span class="sxs-lookup"><span data-stu-id="69e9e-296">{Fatal System Error} The %hs system process terminated unexpectedly with a status of 0x%08x (0x%08x 0x%08x).</span></span> <span data-ttu-id="69e9e-297">O sistema foi desligado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-297">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**dados de erro \_ \_ não \_ aceitos**</span><span class="sxs-lookup"><span data-stu-id="69e9e-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**ERROR\_DATA\_NOT\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-299">592 (0x250)</span><span class="sxs-lookup"><span data-stu-id="69e9e-299">592 (0x250)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-300">{Dados não aceitos} O cliente TDI não pôde manipular os dados recebidos durante uma indicação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-300">{Data Not Accepted} The TDI client could not handle the data received during an indication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**erro \_ de \_ erro de hardware do VDM \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERROR\_VDM\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-302">593 (0x251)</span><span class="sxs-lookup"><span data-stu-id="69e9e-302">593 (0x251)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-303">NTVDM encontrou um erro de hardware.</span><span class="sxs-lookup"><span data-stu-id="69e9e-303">NTVDM encountered a hard error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERRO \_ ao \_ cancelar o \_ tempo limite de driver**</span><span class="sxs-lookup"><span data-stu-id="69e9e-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERROR\_DRIVER\_CANCEL\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-305">594 (0x252)</span><span class="sxs-lookup"><span data-stu-id="69e9e-305">594 (0x252)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-306">{Cancelar tempo limite} O driver% hs não pôde concluir uma solicitação de e/s cancelada no tempo alocado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-306">{Cancel Timeout} The driver %hs failed to complete a cancelled I/O request in the allotted time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**incompatibilidade de mensagem de resposta de erro \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR\_REPLY\_MESSAGE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-308">595 (0x253)</span><span class="sxs-lookup"><span data-stu-id="69e9e-308">595 (0x253)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-309">{Incompatibilidade de mensagem de resposta} Foi feita uma tentativa de responder a uma mensagem de LPC, mas o thread especificado pela ID do cliente na mensagem não estava aguardando essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="69e9e-309">{Reply Message Mismatch} An attempt was made to reply to an LPC message, but the thread specified by the client ID in the message was not waiting on that message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERRO \_ ao \_ perder \_ dados de WRITEBEHIND**</span><span class="sxs-lookup"><span data-stu-id="69e9e-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-311">596 (0x254)</span><span class="sxs-lookup"><span data-stu-id="69e9e-311">596 (0x254)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-312">{Falha na gravação atrasada} O Windows não pôde salvar todos os dados do arquivo% hs.</span><span class="sxs-lookup"><span data-stu-id="69e9e-312">{Delayed Write Failed} Windows was unable to save all the data for the file %hs.</span></span> <span data-ttu-id="69e9e-313">Os dados foram perdidos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-313">The data has been lost.</span></span> <span data-ttu-id="69e9e-314">Esse erro pode ser causado por uma falha de conexão de rede ou de hardware do seu computador.</span><span class="sxs-lookup"><span data-stu-id="69e9e-314">This error may be caused by a failure of your computer hardware or network connection.</span></span> <span data-ttu-id="69e9e-315">Tente salvar este arquivo em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="69e9e-315">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERRO \_ de \_ parâmetros do servidor cliente \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="69e9e-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR\_CLIENT\_SERVER\_PARAMETERS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-317">597 (0x255)</span><span class="sxs-lookup"><span data-stu-id="69e9e-317">597 (0x255)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-318">Os parâmetros passados para o servidor na janela de memória compartilhada do cliente/servidor eram inválidos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-318">The parameter(s) passed to the server in the client/server shared memory window were invalid.</span></span> <span data-ttu-id="69e9e-319">Muitos dados podem ter sido colocados na janela de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-319">Too much data may have been put in the shared memory window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERRO \_ sem \_ \_ fluxo pequeno**</span><span class="sxs-lookup"><span data-stu-id="69e9e-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR\_NOT\_TINY\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-321">598 (0x256)</span><span class="sxs-lookup"><span data-stu-id="69e9e-321">598 (0x256)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-322">O fluxo não é um pequeno fluxo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-322">The stream is not a tiny stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**\_leitura de \_ estouro de pilha de erros \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR\_STACK\_OVERFLOW\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-324">599 (0x257)</span><span class="sxs-lookup"><span data-stu-id="69e9e-324">599 (0x257)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-325">A solicitação deve ser manipulada pelo código de estouro de pilha.</span><span class="sxs-lookup"><span data-stu-id="69e9e-325">The request must be handled by the stack overflow code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERRO ao \_ Converter \_ em \_ grande**</span><span class="sxs-lookup"><span data-stu-id="69e9e-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR\_CONVERT\_TO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-327">600 (0x258)</span><span class="sxs-lookup"><span data-stu-id="69e9e-327">600 (0x258)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-328">Códigos de status internos do OFS indicando como uma operação de alocação é manipulada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-328">Internal OFS status codes indicating how an allocation operation is handled.</span></span> <span data-ttu-id="69e9e-329">Ele é repetido depois que o onode que o contém é movido ou o fluxo de extensão é convertido em um fluxo grande.</span><span class="sxs-lookup"><span data-stu-id="69e9e-329">Either it is retried after the containing onode is moved or the extent stream is converted to a large stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERRO \_ encontrado \_ fora \_ do \_ escopo**</span><span class="sxs-lookup"><span data-stu-id="69e9e-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR\_FOUND\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-331">601 (0x259)</span><span class="sxs-lookup"><span data-stu-id="69e9e-331">601 (0x259)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-332">A tentativa de localizar o objeto encontrou uma correspondência de objeto por ID no volume, mas está fora do escopo do identificador usado para a operação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-332">The attempt to find the object found an object matching by ID on the volume but it is out of the scope of the handle used for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERRO ao \_ alocar \_ Bucket**</span><span class="sxs-lookup"><span data-stu-id="69e9e-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR\_ALLOCATE\_BUCKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-334">602 (0x25A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-334">602 (0x25A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-335">A matriz de buckets deve ser expandida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-335">The bucket array must be grown.</span></span> <span data-ttu-id="69e9e-336">Repita a transação depois de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="69e9e-336">Retry transaction after doing so.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**\_estouro de Marshall de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERROR\_MARSHALL\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-338">603 (0x25B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-338">603 (0x25B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-339">O buffer de Marshalling de usuário/kernel estourou.</span><span class="sxs-lookup"><span data-stu-id="69e9e-339">The user/kernel marshalling buffer has overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERRO \_ de \_ variante inválida**</span><span class="sxs-lookup"><span data-stu-id="69e9e-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR\_INVALID\_VARIANT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-341">604 (0x25C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-341">604 (0x25C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-342">A estrutura variante fornecida contém dados inválidos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-342">The supplied variant structure contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERRO \_ de \_ buffer de compactação insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR\_BAD\_COMPRESSION\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-344">605 (0x25D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-344">605 (0x25D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-345">O buffer especificado contém dados mal formados.</span><span class="sxs-lookup"><span data-stu-id="69e9e-345">The specified buffer contains ill-formed data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**\_falha na auditoria de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR\_AUDIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-347">606 (0x25E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-347">606 (0x25E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-348">{Falha na auditoria} Falha ao tentar gerar uma auditoria de segurança.</span><span class="sxs-lookup"><span data-stu-id="69e9e-348">{Audit Failed} An attempt to generate a security audit failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**resolução do timer de erro \_ \_ \_ não \_ definida**</span><span class="sxs-lookup"><span data-stu-id="69e9e-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**ERROR\_TIMER\_RESOLUTION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-350">607 (0x25F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-350">607 (0x25F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-351">A resolução do temporizador não foi definida anteriormente pelo processo atual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-351">The timer resolution was not previously set by the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERRO \_ de \_ informações de logon insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR\_INSUFFICIENT\_LOGON\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-353">608 (0x260)</span><span class="sxs-lookup"><span data-stu-id="69e9e-353">608 (0x260)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-354">Não há informações de conta suficientes para fazer logon.</span><span class="sxs-lookup"><span data-stu-id="69e9e-354">There is insufficient account information to log you on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERRO \_ de \_ entrada de DLL inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR\_BAD\_DLL\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-356">609 (0x261)</span><span class="sxs-lookup"><span data-stu-id="69e9e-356">609 (0x261)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-357">{Ponto de entrada DLL inválido} A biblioteca de vínculo dinâmico% hs não foi gravada corretamente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-357">{Invalid DLL Entrypoint} The dynamic link library %hs is not written correctly.</span></span> <span data-ttu-id="69e9e-358">O ponteiro de pilha foi deixado em um estado inconsistente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-358">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="69e9e-359">O EntryPoint deve ser declarado como Winapi tenha ou STDCALL.</span><span class="sxs-lookup"><span data-stu-id="69e9e-359">The entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="69e9e-360">Selecione Sim para falhar a carga da DLL.</span><span class="sxs-lookup"><span data-stu-id="69e9e-360">Select YES to fail the DLL load.</span></span> <span data-ttu-id="69e9e-361">Selecione não para continuar a execução.</span><span class="sxs-lookup"><span data-stu-id="69e9e-361">Select NO to continue execution.</span></span> <span data-ttu-id="69e9e-362">Selecionar não pode fazer com que o aplicativo opere incorretamente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-362">Selecting NO may cause the application to operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERRO \_ de \_ ponto de entrada de serviço insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR\_BAD\_SERVICE\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-364">610 (0x262)</span><span class="sxs-lookup"><span data-stu-id="69e9e-364">610 (0x262)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-365">{Ponto de entrada de retorno de serviço inválido} O serviço% hs não foi gravado corretamente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-365">{Invalid Service Callback Entrypoint} The %hs service is not written correctly.</span></span> <span data-ttu-id="69e9e-366">O ponteiro de pilha foi deixado em um estado inconsistente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-366">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="69e9e-367">O ponto de entrada de retorno de chamada deve ser declarado como Winapi tenha ou STDCALL.</span><span class="sxs-lookup"><span data-stu-id="69e9e-367">The callback entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="69e9e-368">A seleção de OK fará com que o serviço continue a operação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-368">Selecting OK will cause the service to continue operation.</span></span> <span data-ttu-id="69e9e-369">No entanto, o processo de serviço pode funcionar incorretamente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-369">However, the service process may operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERRO \_ de \_ endereço IP \_ CONFLICT1**</span><span class="sxs-lookup"><span data-stu-id="69e9e-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR\_IP\_ADDRESS\_CONFLICT1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-371">611 (0x263)</span><span class="sxs-lookup"><span data-stu-id="69e9e-371">611 (0x263)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-372">Há um conflito de endereço IP com outro sistema na rede.</span><span class="sxs-lookup"><span data-stu-id="69e9e-372">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERRO \_ de \_ endereço IP \_ CONFLICT2**</span><span class="sxs-lookup"><span data-stu-id="69e9e-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR\_IP\_ADDRESS\_CONFLICT2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-374">612 (0x264)</span><span class="sxs-lookup"><span data-stu-id="69e9e-374">612 (0x264)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-375">Há um conflito de endereço IP com outro sistema na rede.</span><span class="sxs-lookup"><span data-stu-id="69e9e-375">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_limite de \_ cota de registro de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**ERROR\_REGISTRY\_QUOTA\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-377">613 (0x265)</span><span class="sxs-lookup"><span data-stu-id="69e9e-377">613 (0x265)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-378">{Pouco espaço no registro} O sistema atingiu o tamanho máximo permitido para a parte do sistema do registro.</span><span class="sxs-lookup"><span data-stu-id="69e9e-378">{Low On Registry Space} The system has reached the maximum size allowed for the system part of the registry.</span></span> <span data-ttu-id="69e9e-379">As solicitações de armazenamento adicionais serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="69e9e-379">Additional storage requests will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERRO \_ nenhum \_ retorno de chamada \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="69e9e-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR\_NO\_CALLBACK\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-381">614 (0x266)</span><span class="sxs-lookup"><span data-stu-id="69e9e-381">614 (0x266)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-382">Um serviço do sistema de retorno de chamada de retorno não pode ser executado quando nenhum retorno de chamada está ativo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-382">A callback return system service cannot be executed when no callback is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERRO \_ pwd \_ muito \_ curto**</span><span class="sxs-lookup"><span data-stu-id="69e9e-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR\_PWD\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-384">615 (0x267)</span><span class="sxs-lookup"><span data-stu-id="69e9e-384">615 (0x267)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-385">A senha fornecida é muito curta para atender à política de sua conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="69e9e-385">The password provided is too short to meet the policy of your user account.</span></span> <span data-ttu-id="69e9e-386">Escolha uma senha mais longa.</span><span class="sxs-lookup"><span data-stu-id="69e9e-386">Please choose a longer password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERRO \_ pwd \_ muito \_ recente**</span><span class="sxs-lookup"><span data-stu-id="69e9e-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR\_PWD\_TOO\_RECENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-388">616 (0x268)</span><span class="sxs-lookup"><span data-stu-id="69e9e-388">616 (0x268)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-389">A política da sua conta de usuário não permite que você altere as senhas com muita frequência.</span><span class="sxs-lookup"><span data-stu-id="69e9e-389">The policy of your user account does not allow you to change passwords too frequently.</span></span> <span data-ttu-id="69e9e-390">Isso é feito para impedir que os usuários mudem de volta para uma senha familiar, mas potencialmente descoberta.</span><span class="sxs-lookup"><span data-stu-id="69e9e-390">This is done to prevent users from changing back to a familiar, but potentially discovered, password.</span></span> <span data-ttu-id="69e9e-391">Se você sentir que sua senha foi comprometida, entre em contato com o administrador imediatamente para ter uma nova atribuída.</span><span class="sxs-lookup"><span data-stu-id="69e9e-391">If you feel your password has been compromised then please contact your administrator immediately to have a new one assigned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**conflito de histórico de erro \_ pwd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERROR\_PWD\_HISTORY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-393">617 (0x269)</span><span class="sxs-lookup"><span data-stu-id="69e9e-393">617 (0x269)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-394">Você tentou alterar sua senha para uma que já usou no passado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-394">You have attempted to change your password to one that you have used in the past.</span></span> <span data-ttu-id="69e9e-395">A política da sua conta de usuário não permite isso.</span><span class="sxs-lookup"><span data-stu-id="69e9e-395">The policy of your user account does not allow this.</span></span> <span data-ttu-id="69e9e-396">Selecione uma senha que você não usou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-396">Please select a password that you have not previously used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERRO de \_ \_ compactação sem suporte**</span><span class="sxs-lookup"><span data-stu-id="69e9e-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR\_UNSUPPORTED\_COMPRESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-398">618 (0x26A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-398">618 (0x26A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-399">O formato de compactação especificado não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="69e9e-399">The specified compression format is unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERRO \_ de \_ perfil HW inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR\_INVALID\_HW\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-401">619 (0x26B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-401">619 (0x26B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-402">A configuração do perfil de hardware especificado é inválida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-402">The specified hardware profile configuration is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERRO \_ de \_ \_ caminho de dispositivo PLUGPLAY inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR\_INVALID\_PLUGPLAY\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-404">620 (0x26C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-404">620 (0x26C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-405">O caminho do dispositivo do registro de Plug and Play especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="69e9e-405">The specified Plug and Play registry device path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**\_lista de cotas de erro \_ \_ inconsistente**</span><span class="sxs-lookup"><span data-stu-id="69e9e-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**ERROR\_QUOTA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-407">621 (0x26D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-407">621 (0x26D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-408">A lista de cotas especificada é internamente inconsistente com seu descritor.</span><span class="sxs-lookup"><span data-stu-id="69e9e-408">The specified quota list is internally inconsistent with its descriptor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**\_expiração da avaliação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**ERROR\_EVALUATION\_EXPIRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-410">622 (0x26E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-410">622 (0x26E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-411">{Notificação de avaliação do Windows} O período de avaliação desta instalação do Windows expirou.</span><span class="sxs-lookup"><span data-stu-id="69e9e-411">{Windows Evaluation Notification} The evaluation period for this installation of Windows has expired.</span></span> <span data-ttu-id="69e9e-412">Este sistema será desligado em 1 hora.</span><span class="sxs-lookup"><span data-stu-id="69e9e-412">This system will shutdown in 1 hour.</span></span> <span data-ttu-id="69e9e-413">Para restaurar o acesso a esta instalação do Windows, atualize esta instalação usando uma distribuição licenciada deste produto.</span><span class="sxs-lookup"><span data-stu-id="69e9e-413">To restore access to this installation of Windows, please upgrade this installation using a licensed distribution of this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERRO \_ de \_ \_ realocação de dll ilegal**</span><span class="sxs-lookup"><span data-stu-id="69e9e-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR\_ILLEGAL\_DLL\_RELOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-415">623 (0x26F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-415">623 (0x26F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-416">{Realocação de DLL do sistema ilegal} A DLL do sistema% HS foi realocada na memória.</span><span class="sxs-lookup"><span data-stu-id="69e9e-416">{Illegal System DLL Relocation} The system DLL %hs was relocated in memory.</span></span> <span data-ttu-id="69e9e-417">O aplicativo não será executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-417">The application will not run properly.</span></span> <span data-ttu-id="69e9e-418">A realocação ocorreu porque a DLL% HS ocupava um intervalo de endereços reservado para DLLs de sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="69e9e-418">The relocation occurred because the DLL %hs occupied an address range reserved for Windows system DLLs.</span></span> <span data-ttu-id="69e9e-419">O fornecedor que fornece a DLL deve ser contatado para uma nova DLL.</span><span class="sxs-lookup"><span data-stu-id="69e9e-419">The vendor supplying the DLL should be contacted for a new DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERRO \_ dll \_ init \_ falha ao fazer \_ logoff**</span><span class="sxs-lookup"><span data-stu-id="69e9e-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR\_DLL\_INIT\_FAILED\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-421">624 (0x270)</span><span class="sxs-lookup"><span data-stu-id="69e9e-421">624 (0x270)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-422">{Falha na inicialização da DLL} Falha ao inicializar o aplicativo porque a estação de janela está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-422">{DLL Initialization Failed} The application failed to initialize because the window station is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERRO ao \_ validar a \_ continuação**</span><span class="sxs-lookup"><span data-stu-id="69e9e-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR\_VALIDATE\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-424">625 (0x271)</span><span class="sxs-lookup"><span data-stu-id="69e9e-424">625 (0x271)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-425">O processo de validação precisa continuar na próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="69e9e-425">The validation process needs to continue on to the next step.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERRO \_ sem \_ mais \_ correspondências**</span><span class="sxs-lookup"><span data-stu-id="69e9e-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR\_NO\_MORE\_MATCHES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-427">626 (0x272)</span><span class="sxs-lookup"><span data-stu-id="69e9e-427">626 (0x272)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-428">Não há mais correspondências para a enumeração de índice atual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-428">There are no more matches for the current index enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_conflito de \_ lista de intervalo de erros \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**ERROR\_RANGE\_LIST\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-430">627 (0x273)</span><span class="sxs-lookup"><span data-stu-id="69e9e-430">627 (0x273)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-431">Não foi possível adicionar o intervalo à lista de intervalos devido a um conflito.</span><span class="sxs-lookup"><span data-stu-id="69e9e-431">The range could not be added to the range list because of a conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**incompatibilidade de \_ SID do servidor de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR\_SERVER\_SID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-433">628 (0x274)</span><span class="sxs-lookup"><span data-stu-id="69e9e-433">628 (0x274)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-434">O processo do servidor está sendo executado sob um SID diferente daquele exigido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-434">The server process is running under a SID different than that required by client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERRO não é possível \_ \_ habilitar \_ \_ somente negar**</span><span class="sxs-lookup"><span data-stu-id="69e9e-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR\_CANT\_ENABLE\_DENY\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-436">629 (0x275)</span><span class="sxs-lookup"><span data-stu-id="69e9e-436">629 (0x275)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-437">Um grupo marcado como uso somente para negar não pode ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-437">A group marked use for deny only cannot be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERRO ao \_ flutuar \_ várias \_ falhas**</span><span class="sxs-lookup"><span data-stu-id="69e9e-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR\_FLOAT\_MULTIPLE\_FAULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-439">630 (0x276)</span><span class="sxs-lookup"><span data-stu-id="69e9e-439">630 (0x276)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-440">Exception Várias falhas de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="69e9e-440">{EXCEPTION} Multiple floating point faults.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERRO ao \_ flutuar \_ várias \_ interceptações**</span><span class="sxs-lookup"><span data-stu-id="69e9e-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR\_FLOAT\_MULTIPLE\_TRAPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-442">631 (0x277)</span><span class="sxs-lookup"><span data-stu-id="69e9e-442">631 (0x277)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-443">Exception Várias interceptações de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="69e9e-443">{EXCEPTION} Multiple floating point traps.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERRO \_ NOinterface**</span><span class="sxs-lookup"><span data-stu-id="69e9e-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR\_NOINTERFACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-445">632 (0x278)</span><span class="sxs-lookup"><span data-stu-id="69e9e-445">632 (0x278)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-446">Não há suporte para a interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-446">The requested interface is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**\_ \_ falha no suspensão do driver de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR\_DRIVER\_FAILED\_SLEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-448">633 (0x279)</span><span class="sxs-lookup"><span data-stu-id="69e9e-448">633 (0x279)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-449">{Falha no sistema em espera} O driver% hs não dá suporte ao modo de espera.</span><span class="sxs-lookup"><span data-stu-id="69e9e-449">{System Standby Failed} The driver %hs does not support standby mode.</span></span> <span data-ttu-id="69e9e-450">A atualização deste driver pode permitir que o sistema vá para o modo de espera.</span><span class="sxs-lookup"><span data-stu-id="69e9e-450">Updating this driver may allow the system to go to standby mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERRO \_ \_ arquivo de sistema corrompido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR\_CORRUPT\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-452">634 (0x27A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-452">634 (0x27A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-453">O arquivo de sistema %1 se tornou corrompido e foi substituído.</span><span class="sxs-lookup"><span data-stu-id="69e9e-453">The system file %1 has become corrupt and has been replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**\_mínimo de compromisso de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERROR\_COMMITMENT\_MINIMUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-455">635 (0x27B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-455">635 (0x27B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-456">{Memória virtual mínima muito baixa} O sistema está com pouca memória virtual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-456">{Virtual Memory Minimum Too Low} Your system is low on virtual memory.</span></span> <span data-ttu-id="69e9e-457">O Windows está aumentando o tamanho do arquivo de paginação da memória virtual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-457">Windows is increasing the size of your virtual memory paging file.</span></span> <span data-ttu-id="69e9e-458">Durante esse processo, as solicitações de memória para alguns aplicativos podem ser negadas.</span><span class="sxs-lookup"><span data-stu-id="69e9e-458">During this process, memory requests for some applications may be denied.</span></span> <span data-ttu-id="69e9e-459">Para obter mais informações, consulte a ajuda.</span><span class="sxs-lookup"><span data-stu-id="69e9e-459">For more information, see Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERRO \_ de \_ enumeração de reinício de PNP \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR\_PNP\_RESTART\_ENUMERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-461">636 (0x27C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-461">636 (0x27C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-462">Um dispositivo foi removido; portanto, A enumeração deve ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-462">A device was removed so enumeration must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERRO \_ de \_ \_ assinatura inadequada da imagem do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERROR\_SYSTEM\_IMAGE\_BAD\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-464">637 (0x27D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-464">637 (0x27D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-465">{Erro fatal do sistema} A imagem do sistema% s não está assinada corretamente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-465">{Fatal System Error} The system image %s is not properly signed.</span></span> <span data-ttu-id="69e9e-466">O arquivo foi substituído pelo arquivo assinado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-466">The file has been replaced with the signed file.</span></span> <span data-ttu-id="69e9e-467">O sistema foi desligado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-467">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERRO \_ de \_ reinicialização de PNP \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="69e9e-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR\_PNP\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-469">638 (0x27E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-469">638 (0x27E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-470">O dispositivo não será iniciado sem uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="69e9e-470">Device will not start without a reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERRO \_ de \_ energia insuficiente**</span><span class="sxs-lookup"><span data-stu-id="69e9e-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR\_INSUFFICIENT\_POWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-472">639 (0x27F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-472">639 (0x27F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-473">Não há energia suficiente para concluir a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-473">There is not enough power to complete the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERRO \_ de \_ várias \_ violações de falha**</span><span class="sxs-lookup"><span data-stu-id="69e9e-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR\_MULTIPLE\_FAULT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-475">640 (0x280)</span><span class="sxs-lookup"><span data-stu-id="69e9e-475">640 (0x280)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-476">ERRO \_ de \_ várias \_ violações de falha</span><span class="sxs-lookup"><span data-stu-id="69e9e-476">ERROR\_MULTIPLE\_FAULT\_VIOLATION</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERRO \_ de \_ desligamento do sistema**</span><span class="sxs-lookup"><span data-stu-id="69e9e-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-478">641 (0x281)</span><span class="sxs-lookup"><span data-stu-id="69e9e-478">641 (0x281)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-479">O sistema está em processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="69e9e-479">The system is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**porta de erro \_ \_ não \_ definida**</span><span class="sxs-lookup"><span data-stu-id="69e9e-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**ERROR\_PORT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-481">642 (0x282)</span><span class="sxs-lookup"><span data-stu-id="69e9e-481">642 (0x282)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-482">Foi feita uma tentativa de remover DebugPort de processos, mas uma porta ainda não estava associada ao processo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-482">An attempt to remove a processes DebugPort was made, but a port was not already associated with the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERRO \_ \_ na verificação da versão DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR\_DS\_VERSION\_CHECK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-484">643 (0x283)</span><span class="sxs-lookup"><span data-stu-id="69e9e-484">643 (0x283)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-485">Esta versão do Windows não é compatível com a versão de comportamento da floresta de diretório, domínio ou controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="69e9e-485">This version of Windows is not compatible with the behavior version of directory forest, domain or domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**intervalo de erros \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**ERROR\_RANGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-487">644 (0x284)</span><span class="sxs-lookup"><span data-stu-id="69e9e-487">644 (0x284)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-488">O intervalo especificado não foi encontrado na lista de intervalos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-488">The specified range could not be found in the range list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERRO \_ não é um \_ \_ Driver de modo seguro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR\_NOT\_SAFE\_MODE\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-490">646 (0x286)</span><span class="sxs-lookup"><span data-stu-id="69e9e-490">646 (0x286)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-491">O driver não foi carregado porque o sistema está sendo inicializado no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="69e9e-491">The driver was not loaded because the system is booting into safe mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERRO \_ de \_ entrada de driver com falha \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR\_FAILED\_DRIVER\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-493">647 (0x287)</span><span class="sxs-lookup"><span data-stu-id="69e9e-493">647 (0x287)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-494">O driver não foi carregado porque falhou em sua chamada de inicialização.</span><span class="sxs-lookup"><span data-stu-id="69e9e-494">The driver was not loaded because it failed its initialization call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**\_erro de \_ enumeração de dispositivo de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**ERROR\_DEVICE\_ENUMERATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-496">648 (0x288)</span><span class="sxs-lookup"><span data-stu-id="69e9e-496">648 (0x288)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-497">"% Hs" encontrou um erro ao aplicar energia ou ler a configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-497">The "%hs" encountered an error while applying power or reading the device configuration.</span></span> <span data-ttu-id="69e9e-498">Isso pode ser causado por uma falha de seu hardware ou por uma conexão ruim.</span><span class="sxs-lookup"><span data-stu-id="69e9e-498">This may be caused by a failure of your hardware or by a poor connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ponto de montagem do erro \_ \_ \_ não \_ resolvido**</span><span class="sxs-lookup"><span data-stu-id="69e9e-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ERROR\_MOUNT\_POINT\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-500">649 (0x289)</span><span class="sxs-lookup"><span data-stu-id="69e9e-500">649 (0x289)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-501">A operação de criação falhou porque o nome continha pelo menos um ponto de montagem que é resolvido para um volume ao qual o objeto de dispositivo especificado não está anexado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-501">The create operation failed because the name contained at least one mount point which resolves to a volume to which the specified device object is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERRO \_ de \_ \_ parâmetro de objeto de dispositivo inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR\_INVALID\_DEVICE\_OBJECT\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-503">650 (0x28A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-503">650 (0x28A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-504">O parâmetro de objeto do dispositivo não é um objeto de dispositivo válido ou não está anexado ao volume especificado pelo nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-504">The device object parameter is either not a valid device object or is not attached to the volume specified by the file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERRO de \_ MCA \_ ocorrido**</span><span class="sxs-lookup"><span data-stu-id="69e9e-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR\_MCA\_OCCURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-506">651 (0x28B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-506">651 (0x28B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-507">Ocorreu um erro de verificação de máquina.</span><span class="sxs-lookup"><span data-stu-id="69e9e-507">A Machine Check Error has occurred.</span></span> <span data-ttu-id="69e9e-508">Consulte o log de eventos do sistema para obter informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="69e9e-508">Please check the system eventlog for additional information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**\_erro de \_ banco de dados de driver de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**ERROR\_DRIVER\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-510">652 (0x28C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-510">652 (0x28C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-511">Erro \[ %2 ao \] processar o banco de dados do driver.</span><span class="sxs-lookup"><span data-stu-id="69e9e-511">There was error \[%2\] processing the driver database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**o hive do sistema de erro é \_ \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="69e9e-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERROR\_SYSTEM\_HIVE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-513">653 (0x28D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-513">653 (0x28D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-514">O tamanho do hive do sistema excedeu seu limite.</span><span class="sxs-lookup"><span data-stu-id="69e9e-514">System hive size has exceeded its limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**\_ \_ falha no \_ \_ descarregamento anterior do driver de erro**</span><span class="sxs-lookup"><span data-stu-id="69e9e-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR\_DRIVER\_FAILED\_PRIOR\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-516">654 (0x28E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-516">654 (0x28E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-517">Não foi possível carregar o driver porque uma versão anterior do driver ainda está na memória.</span><span class="sxs-lookup"><span data-stu-id="69e9e-517">The driver could not be loaded because a previous version of the driver is still in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERRO \_ VOLSNAP \_ preparar \_ hibernação**</span><span class="sxs-lookup"><span data-stu-id="69e9e-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR\_VOLSNAP\_PREPARE\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-519">655 (0x28F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-519">655 (0x28F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-520">{Serviço de Cópias de Sombra de Volume} Aguarde enquanto o Serviço de Cópias de Sombra de Volume prepara o volume% hs para hibernação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-520">{Volume Shadow Copy Service} Please wait while the Volume Shadow Copy Service prepares volume %hs for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**\_falha de hibernação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR\_HIBERNATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-522">656 (0x290)</span><span class="sxs-lookup"><span data-stu-id="69e9e-522">656 (0x290)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-523">O sistema falhou ao hibernar (o código de erro é% HS).</span><span class="sxs-lookup"><span data-stu-id="69e9e-523">The system has failed to hibernate (The error code is %hs).</span></span> <span data-ttu-id="69e9e-524">A hibernação será desabilitada até que o sistema seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-524">Hibernation will be disabled until the system is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERRO \_ pwd \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="69e9e-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR\_PWD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-526">657 (0x291)</span><span class="sxs-lookup"><span data-stu-id="69e9e-526">657 (0x291)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-527">A senha fornecida é muito longa para atender à política de sua conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="69e9e-527">The password provided is too long to meet the policy of your user account.</span></span> <span data-ttu-id="69e9e-528">Escolha uma senha mais curta.</span><span class="sxs-lookup"><span data-stu-id="69e9e-528">Please choose a shorter password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_limitação do \_ sistema de arquivos de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**ERROR\_FILE\_SYSTEM\_LIMITATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-530">665 (0x299)</span><span class="sxs-lookup"><span data-stu-id="69e9e-530">665 (0x299)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-531">Não foi possível concluir a operação solicitada devido a uma limitação do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-531">The requested operation could not be completed due to a file system limitation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**\_falha na asserção de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERROR\_ASSERTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-533">668 (0x29C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-533">668 (0x29C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-534">Ocorreu uma falha de asserção.</span><span class="sxs-lookup"><span data-stu-id="69e9e-534">An assertion failure has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**erro de \_ ACPI \_ erro**</span><span class="sxs-lookup"><span data-stu-id="69e9e-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**ERROR\_ACPI\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-536">669 (0x29D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-536">669 (0x29D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-537">Ocorreu um erro no subsistema ACPI.</span><span class="sxs-lookup"><span data-stu-id="69e9e-537">An error occurred in the ACPI subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERRO \_ de \_ asserção Wow**</span><span class="sxs-lookup"><span data-stu-id="69e9e-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR\_WOW\_ASSERTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-539">670 (0x29E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-539">670 (0x29E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-540">Erro de asserção WOW.</span><span class="sxs-lookup"><span data-stu-id="69e9e-540">WOW Assertion Error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERRO \_ PNP de uma \_ \_ tabela MPS inadequada \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR\_PNP\_BAD\_MPS\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-542">671 (0x29F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-542">671 (0x29F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-543">Um dispositivo está ausente na tabela MPS do BIOS do sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-543">A device is missing in the system BIOS MPS table.</span></span> <span data-ttu-id="69e9e-544">Este dispositivo não será usado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-544">This device will not be used.</span></span> <span data-ttu-id="69e9e-545">Entre em contato com o fornecedor do sistema para obter a atualização do BIOS do sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-545">Please contact your system vendor for system BIOS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERRO \_ \_ na conversão de PNP \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR\_PNP\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-547">672 (0x2A0)</span><span class="sxs-lookup"><span data-stu-id="69e9e-547">672 (0x2A0)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-548">Um tradutor não pôde converter os recursos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-548">A translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERRO \_ \_ na conversão de IRQ de PNP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR\_PNP\_IRQ\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-550">673 (0x2A1)</span><span class="sxs-lookup"><span data-stu-id="69e9e-550">673 (0x2A1)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-551">Um tradutor de IRQ falhou ao converter recursos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-551">A IRQ translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERRO de \_ ID de PNP \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR\_PNP\_INVALID\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-553">674 (0x2A2)</span><span class="sxs-lookup"><span data-stu-id="69e9e-553">674 (0x2A2)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-554">O driver %2 retornou uma ID inválida para um dispositivo filho (%3).</span><span class="sxs-lookup"><span data-stu-id="69e9e-554">Driver %2 returned invalid ID for a child device (%3).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERRO \_ do \_ depurador do sistema de ativação \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR\_WAKE\_SYSTEM\_DEBUGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-556">675 (0x2A3)</span><span class="sxs-lookup"><span data-stu-id="69e9e-556">675 (0x2A3)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-557">{Kernel Debugger ativado} o depurador do sistema foi ativado por uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="69e9e-557">{Kernel Debugger Awakened} the system debugger was awakened by an interrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**\_identificadores de erro \_ fechados**</span><span class="sxs-lookup"><span data-stu-id="69e9e-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**ERROR\_HANDLES\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-559">676 (0x2A4)</span><span class="sxs-lookup"><span data-stu-id="69e9e-559">676 (0x2A4)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-560">{Identificadores fechados} Identificadores para objetos foram fechados automaticamente como resultado da operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-560">{Handles Closed} Handles to objects have been automatically closed as a result of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**\_informações incorretas sobre o erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERROR\_EXTRANEOUS\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-562">677 (0x2A5)</span><span class="sxs-lookup"><span data-stu-id="69e9e-562">677 (0x2A5)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-563">{Excesso de informações} A lista de controle de acesso (ACL) especificada continha mais informações do que o esperado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-563">{Too Much Information} The specified access control list (ACL) contained more information than was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**confirmação de RXACT de erro \_ \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="69e9e-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR\_RXACT\_COMMIT\_NECESSARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-565">678 (0x2A6)</span><span class="sxs-lookup"><span data-stu-id="69e9e-565">678 (0x2A6)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-566">Esse status de nível de aviso indica que o estado da transação já existe para a subárvore do registro, mas que uma confirmação de transação foi anulada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-566">This warning level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="69e9e-567">A confirmação não foi concluída, mas não foi revertida (portanto, ela ainda pode ser confirmada se desejado).</span><span class="sxs-lookup"><span data-stu-id="69e9e-567">The commit has NOT been completed, but has not been rolled back either (so it may still be committed if desired).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_verificação de mídia de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**ERROR\_MEDIA\_CHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-569">679 (0x2A7)</span><span class="sxs-lookup"><span data-stu-id="69e9e-569">679 (0x2A7)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-570">{Mídia alterada} A mídia pode ter sido alterada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-570">{Media Changed} The media may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**substituição de GUID de erro \_ \_ \_ feita**</span><span class="sxs-lookup"><span data-stu-id="69e9e-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**ERROR\_GUID\_SUBSTITUTION\_MADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-572">680 (0x2A8)</span><span class="sxs-lookup"><span data-stu-id="69e9e-572">680 (0x2A8)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-573">{Substituição de GUID} Durante a tradução de um identificador global (GUID) para uma ID de segurança (SID) do Windows, nenhum prefixo GUID definido administrativamente foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-573">{GUID Substitution} During the translation of a global identifier (GUID) to a Windows security ID (SID), no administratively-defined GUID prefix was found.</span></span> <span data-ttu-id="69e9e-574">Um prefixo substituto foi usado, o que não comprometerá a segurança do sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-574">A substitute prefix was used, which will not compromise system security.</span></span> <span data-ttu-id="69e9e-575">No entanto, isso pode fornecer um acesso mais restritivo do que o pretendido.</span><span class="sxs-lookup"><span data-stu-id="69e9e-575">However, this may provide a more restrictive access than intended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERRO \_ interrompido \_ em \_ SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="69e9e-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR\_STOPPED\_ON\_SYMLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-577">681 (0x2A9)</span><span class="sxs-lookup"><span data-stu-id="69e9e-577">681 (0x2A9)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-578">A operação de criação parou depois de atingir um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="69e9e-578">The create operation stopped after reaching a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERRO \_ LONGJUMP**</span><span class="sxs-lookup"><span data-stu-id="69e9e-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR\_LONGJUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-580">682 (0x2AA)</span><span class="sxs-lookup"><span data-stu-id="69e9e-580">682 (0x2AA)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-581">Um salto longo foi executado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-581">A long jump has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERRO \_ PLUGPLAY \_ consulta \_ vetada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR\_PLUGPLAY\_QUERY\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-583">683 (0x2AB)</span><span class="sxs-lookup"><span data-stu-id="69e9e-583">683 (0x2AB)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-584">A operação de consulta de Plug and Play não foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-584">The Plug and Play query operation was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**reliberação de erro de \_ \_ desconsolidação**</span><span class="sxs-lookup"><span data-stu-id="69e9e-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR\_UNWIND\_CONSOLIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-586">684 (0x2AC)</span><span class="sxs-lookup"><span data-stu-id="69e9e-586">684 (0x2AC)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-587">Uma consolidação de quadros foi executada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-587">A frame consolidation has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**\_hive do registro de erro \_ \_ recuperado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR\_REGISTRY\_HIVE\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-589">685 (0x2AD)</span><span class="sxs-lookup"><span data-stu-id="69e9e-589">685 (0x2AD)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-590">{O hive do registro foi recuperado} Hive do registro (arquivo):% HS foi corrompido e foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-590">{Registry Hive Recovered} Registry hive (file): %hs was corrupted and it has been recovered.</span></span> <span data-ttu-id="69e9e-591">Alguns dados podem ter sido perdidos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-591">Some data might have been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**DLL de erro \_ \_ pode \_ ser \_ inseguro**</span><span class="sxs-lookup"><span data-stu-id="69e9e-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**ERROR\_DLL\_MIGHT\_BE\_INSECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-593">686 (0x2AE)</span><span class="sxs-lookup"><span data-stu-id="69e9e-593">686 (0x2AE)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-594">O aplicativo está tentando executar o código executável do módulo% hs.</span><span class="sxs-lookup"><span data-stu-id="69e9e-594">The application is attempting to run executable code from the module %hs.</span></span> <span data-ttu-id="69e9e-595">Isso pode ser inseguro.</span><span class="sxs-lookup"><span data-stu-id="69e9e-595">This may be insecure.</span></span> <span data-ttu-id="69e9e-596">Uma alternativa,% HS, está disponível.</span><span class="sxs-lookup"><span data-stu-id="69e9e-596">An alternative, %hs, is available.</span></span> <span data-ttu-id="69e9e-597">O aplicativo deve usar o módulo seguro% HS?</span><span class="sxs-lookup"><span data-stu-id="69e9e-597">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**DLL de erro \_ \_ pode \_ ser \_ incompatível**</span><span class="sxs-lookup"><span data-stu-id="69e9e-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**ERROR\_DLL\_MIGHT\_BE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-599">687 (0x2AF)</span><span class="sxs-lookup"><span data-stu-id="69e9e-599">687 (0x2AF)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-600">O aplicativo está carregando o código executável do módulo% hs.</span><span class="sxs-lookup"><span data-stu-id="69e9e-600">The application is loading executable code from the module %hs.</span></span> <span data-ttu-id="69e9e-601">Isso é seguro, mas pode ser incompatível com as versões anteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="69e9e-601">This is secure, but may be incompatible with previous releases of the operating system.</span></span> <span data-ttu-id="69e9e-602">Uma alternativa,% HS, está disponível.</span><span class="sxs-lookup"><span data-stu-id="69e9e-602">An alternative, %hs, is available.</span></span> <span data-ttu-id="69e9e-603">O aplicativo deve usar o módulo seguro% HS?</span><span class="sxs-lookup"><span data-stu-id="69e9e-603">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERRO \_ de \_ exceção DBG \_ não \_ tratada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR\_DBG\_EXCEPTION\_NOT\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-605">688 (0x2B0)</span><span class="sxs-lookup"><span data-stu-id="69e9e-605">688 (0x2B0)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-606">O depurador não resolveu a exceção.</span><span class="sxs-lookup"><span data-stu-id="69e9e-606">Debugger did not handle the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERRO \_ DBG \_ responder \_ mais tarde**</span><span class="sxs-lookup"><span data-stu-id="69e9e-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR\_DBG\_REPLY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-608">689 (0x2B1)</span><span class="sxs-lookup"><span data-stu-id="69e9e-608">689 (0x2B1)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-609">O depurador será respondido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="69e9e-609">Debugger will reply later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERRO \_ DBG \_ não é possível \_ \_ fornecer \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="69e9e-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR\_DBG\_UNABLE\_TO\_PROVIDE\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-611">690 (0x2B2)</span><span class="sxs-lookup"><span data-stu-id="69e9e-611">690 (0x2B2)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-612">O depurador não pode fornecer identificador.</span><span class="sxs-lookup"><span data-stu-id="69e9e-612">Debugger cannot provide handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERRO \_ de \_ término do \_ thread DBG**</span><span class="sxs-lookup"><span data-stu-id="69e9e-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR\_DBG\_TERMINATE\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-614">691 (0x2B3)</span><span class="sxs-lookup"><span data-stu-id="69e9e-614">691 (0x2B3)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-615">Thread encerrado pelo depurador.</span><span class="sxs-lookup"><span data-stu-id="69e9e-615">Debugger terminated thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERRO \_ de \_ finalizar processo de DBG \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR\_DBG\_TERMINATE\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-617">692 (0x2B4)</span><span class="sxs-lookup"><span data-stu-id="69e9e-617">692 (0x2B4)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-618">Processo finalizado pelo depurador.</span><span class="sxs-lookup"><span data-stu-id="69e9e-618">Debugger terminated process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERRO \_ de \_ controle DBG \_ C**</span><span class="sxs-lookup"><span data-stu-id="69e9e-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR\_DBG\_CONTROL\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-620">693 (0x2B5)</span><span class="sxs-lookup"><span data-stu-id="69e9e-620">693 (0x2B5)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-621">O depurador obteve o controle C.</span><span class="sxs-lookup"><span data-stu-id="69e9e-621">Debugger got control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERRO \_ DBG \_ com exceção \_ C**</span><span class="sxs-lookup"><span data-stu-id="69e9e-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR\_DBG\_PRINTEXCEPTION\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-623">694 (0x2B6)</span><span class="sxs-lookup"><span data-stu-id="69e9e-623">694 (0x2B6)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-624">O depurador imprimiu a exceção no controle C.</span><span class="sxs-lookup"><span data-stu-id="69e9e-624">Debugger printed exception on control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERRO \_ DBG \_ RIPEXCEPTION**</span><span class="sxs-lookup"><span data-stu-id="69e9e-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR\_DBG\_RIPEXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-626">695 (0x2B7)</span><span class="sxs-lookup"><span data-stu-id="69e9e-626">695 (0x2B7)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-627">O depurador recebeu uma exceção RIP.</span><span class="sxs-lookup"><span data-stu-id="69e9e-627">Debugger received RIP exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERRO \_ de \_ quebra de controle DBG \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR\_DBG\_CONTROL\_BREAK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-629">696 (0x2B8)</span><span class="sxs-lookup"><span data-stu-id="69e9e-629">696 (0x2B8)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-630">O depurador recebeu uma quebra de controle.</span><span class="sxs-lookup"><span data-stu-id="69e9e-630">Debugger received control break.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERRO \_ de \_ exceção de comando DBG \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR\_DBG\_COMMAND\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-632">697 (0x2B9)</span><span class="sxs-lookup"><span data-stu-id="69e9e-632">697 (0x2B9)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-633">Exceção de comunicação de comando do depurador.</span><span class="sxs-lookup"><span data-stu-id="69e9e-633">Debugger command communication exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**o \_ nome do objeto de erro \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="69e9e-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**ERROR\_OBJECT\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-635">698 (0x2BA)</span><span class="sxs-lookup"><span data-stu-id="69e9e-635">698 (0x2BA)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-636">{Objeto existe} Foi feita uma tentativa de criar um objeto e o nome do objeto já existia.</span><span class="sxs-lookup"><span data-stu-id="69e9e-636">{Object Exists} An attempt was made to create an object and the object name already existed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**o \_ thread de erro \_ foi \_ suspenso**</span><span class="sxs-lookup"><span data-stu-id="69e9e-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**ERROR\_THREAD\_WAS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-638">699 (0x2BB)</span><span class="sxs-lookup"><span data-stu-id="69e9e-638">699 (0x2BB)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-639">{Thread suspenso} Uma terminação de thread ocorreu enquanto o thread estava suspenso.</span><span class="sxs-lookup"><span data-stu-id="69e9e-639">{Thread Suspended} A thread termination occurred while the thread was suspended.</span></span> <span data-ttu-id="69e9e-640">O thread foi retomado e o encerramento foi continuado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-640">The thread was resumed, and termination proceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**\_imagem \_ de erro não \_ na \_ base**</span><span class="sxs-lookup"><span data-stu-id="69e9e-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**ERROR\_IMAGE\_NOT\_AT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-642">700 (0x2BC)</span><span class="sxs-lookup"><span data-stu-id="69e9e-642">700 (0x2BC)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-643">{Imagem realocada} Não foi possível mapear um arquivo de imagem no endereço especificado no arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="69e9e-643">{Image Relocated} An image file could not be mapped at the address specified in the image file.</span></span> <span data-ttu-id="69e9e-644">As correções locais devem ser executadas nesta imagem.</span><span class="sxs-lookup"><span data-stu-id="69e9e-644">Local fixups must be performed on this image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERRO \_ RXACT \_ estado \_ criado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR\_RXACT\_STATE\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-646">701 (0x2BD)</span><span class="sxs-lookup"><span data-stu-id="69e9e-646">701 (0x2BD)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-647">Esse status de nível informativo indica que um estado de transação de subárvore do registro especificado ainda não existia e teve que ser criado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-647">This informational level status indicates that a specified registry sub-tree transaction state did not yet exist and had to be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_notificação de segmento de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**ERROR\_SEGMENT\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-649">702 (0x2BE)</span><span class="sxs-lookup"><span data-stu-id="69e9e-649">702 (0x2BE)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-650">{Carga do segmento} Uma máquina virtual de DOS (VDM) está carregando, descarregando ou movendo uma imagem de segmento de programa do MS-DOS ou Win16.</span><span class="sxs-lookup"><span data-stu-id="69e9e-650">{Segment Load} A virtual DOS machine (VDM) is loading, unloading, or moving an MS-DOS or Win16 program segment image.</span></span> <span data-ttu-id="69e9e-651">Uma exceção é gerada para que um depurador possa carregar, descarregar ou rastrear símbolos e pontos de interrupção nesses segmentos de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="69e9e-651">An exception is raised so a debugger can load, unload or track symbols and breakpoints within these 16-bit segments.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERRO \_ de \_ diretório atual insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR\_BAD\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-653">703 (0x2BF)</span><span class="sxs-lookup"><span data-stu-id="69e9e-653">703 (0x2BF)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-654">{Diretório atual inválido} O processo não pode mudar para o diretório atual de inicialização% hs.</span><span class="sxs-lookup"><span data-stu-id="69e9e-654">{Invalid Current Directory} The process cannot switch to the startup current directory %hs.</span></span> <span data-ttu-id="69e9e-655">Selecione OK para definir o diretório atual como% HS ou selecione Cancelar para sair.</span><span class="sxs-lookup"><span data-stu-id="69e9e-655">Select OK to set current directory to %hs, or select CANCEL to exit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERRO \_ ft \_ Read \_ Recovery \_ do \_ backup**</span><span class="sxs-lookup"><span data-stu-id="69e9e-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR\_FT\_READ\_RECOVERY\_FROM\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-657">704 (0x2C0)</span><span class="sxs-lookup"><span data-stu-id="69e9e-657">704 (0x2C0)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-658">{Leitura redundante} Para atender a uma solicitação de leitura, o sistema de arquivos tolerante a falhas do NT leu com êxito os dados solicitados de uma cópia redundante.</span><span class="sxs-lookup"><span data-stu-id="69e9e-658">{Redundant Read} To satisfy a read request, the NT fault-tolerant file system successfully read the requested data from a redundant copy.</span></span> <span data-ttu-id="69e9e-659">Isso foi feito porque o sistema de arquivos encontrou uma falha em um membro do volume tolerante a falhas, mas não pôde reatribuir a área com falha do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-659">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was unable to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERRO \_ ft \_ de \_ recuperação de gravação**</span><span class="sxs-lookup"><span data-stu-id="69e9e-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR\_FT\_WRITE\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-661">705 (0x2C1)</span><span class="sxs-lookup"><span data-stu-id="69e9e-661">705 (0x2C1)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-662">{Gravação redundante} Para atender a uma solicitação de gravação, o sistema de arquivos tolerante a falhas do NT escreveu com êxito uma cópia redundante das informações.</span><span class="sxs-lookup"><span data-stu-id="69e9e-662">{Redundant Write} To satisfy a write request, the NT fault-tolerant file system successfully wrote a redundant copy of the information.</span></span> <span data-ttu-id="69e9e-663">Isso foi feito porque o sistema de arquivos encontrou uma falha em um membro do volume tolerante a falhas, mas não pôde reatribuir a área com falha do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-663">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was not able to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**tipo de máquina de imagem de erro \_ \_ \_ \_ incompatível**</span><span class="sxs-lookup"><span data-stu-id="69e9e-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-665">706 (0x2C2)</span><span class="sxs-lookup"><span data-stu-id="69e9e-665">706 (0x2C2)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-666">{Tipo de computador não compatível} O arquivo de imagem% HS é válido, mas é para um tipo de computador diferente do computador atual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-666">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span> <span data-ttu-id="69e9e-667">Selecione OK para continuar ou cancelar para falhar a carga da DLL.</span><span class="sxs-lookup"><span data-stu-id="69e9e-667">Select OK to continue, or CANCEL to fail the DLL load.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERRO ao \_ receber \_ parcial**</span><span class="sxs-lookup"><span data-stu-id="69e9e-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR\_RECEIVE\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-669">707 (0x2C3)</span><span class="sxs-lookup"><span data-stu-id="69e9e-669">707 (0x2C3)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-670">{Dados parciais recebidos} O transporte de rede retornou dados parciais para seu cliente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-670">{Partial Data Received} The network transport returned partial data to its client.</span></span> <span data-ttu-id="69e9e-671">Os dados restantes serão enviados mais tarde.</span><span class="sxs-lookup"><span data-stu-id="69e9e-671">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERRO ao \_ receber \_ acelerado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR\_RECEIVE\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-673">708 (0x2C4)</span><span class="sxs-lookup"><span data-stu-id="69e9e-673">708 (0x2C4)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-674">{Dados emitidos recebidos} O transporte de rede retornou dados para seu cliente que foi marcado como emitido pelo sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="69e9e-674">{Expedited Data Received} The network transport returned data to its client that was marked as expedited by the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERRO \_ ao \_ receber \_ acelerado parcial**</span><span class="sxs-lookup"><span data-stu-id="69e9e-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR\_RECEIVE\_PARTIAL\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-676">709 (0x2C5)</span><span class="sxs-lookup"><span data-stu-id="69e9e-676">709 (0x2C5)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-677">{Dados parciais expedidos recebidos} O transporte de rede retornou dados parciais para seu cliente e esses dados foram marcados como emitidos pelo sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="69e9e-677">{Partial Expedited Data Received} The network transport returned partial data to its client and this data was marked as expedited by the remote system.</span></span> <span data-ttu-id="69e9e-678">Os dados restantes serão enviados mais tarde.</span><span class="sxs-lookup"><span data-stu-id="69e9e-678">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**evento de erro \_ \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="69e9e-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**ERROR\_EVENT\_DONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-680">710 (0x2C6)</span><span class="sxs-lookup"><span data-stu-id="69e9e-680">710 (0x2C6)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-681">{Evento TDI concluído} A indicação de TDI foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="69e9e-681">{TDI Event Done} The TDI indication has completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**evento de erro \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="69e9e-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**ERROR\_EVENT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-683">711 (0x2C7)</span><span class="sxs-lookup"><span data-stu-id="69e9e-683">711 (0x2C7)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-684">{Evento TDI pendente} A indicação de TDI entrou no estado pendente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-684">{TDI Event Pending} The TDI indication has entered the pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERRO ao \_ verificar o \_ sistema de arquivos \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR\_CHECKING\_FILE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-686">712 (0x2C8)</span><span class="sxs-lookup"><span data-stu-id="69e9e-686">712 (0x2C8)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-687">Verificando o sistema de arquivos em% wZ.</span><span class="sxs-lookup"><span data-stu-id="69e9e-687">Checking file system on %wZ.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERRO \_ fatal do \_ aplicativo de \_ saída**</span><span class="sxs-lookup"><span data-stu-id="69e9e-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR\_FATAL\_APP\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-689">713 (0x2C9)</span><span class="sxs-lookup"><span data-stu-id="69e9e-689">713 (0x2C9)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-690">{Saída fatal do aplicativo}% hs.</span><span class="sxs-lookup"><span data-stu-id="69e9e-690">{Fatal Application Exit} %hs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**identificador de erro \_ predefinido \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**ERROR\_PREDEFINED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-692">714 (0x2CA)</span><span class="sxs-lookup"><span data-stu-id="69e9e-692">714 (0x2CA)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-693">A chave do Registro especificada é referenciada por um identificador predefinido.</span><span class="sxs-lookup"><span data-stu-id="69e9e-693">The specified registry key is referenced by a predefined handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERRO \_ \_ desbloqueado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR\_WAS\_UNLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-695">715 (0x2CB)</span><span class="sxs-lookup"><span data-stu-id="69e9e-695">715 (0x2CB)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-696">{Página desbloqueada} A proteção de página de uma página bloqueada foi alterada para ' sem acesso ' e a página foi desbloqueada da memória e do processo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-696">{Page Unlocked} The page protection of a locked page was changed to 'No Access' and the page was unlocked from memory and from the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_notificação do serviço de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**ERROR\_SERVICE\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-698">716 (0x2CC)</span><span class="sxs-lookup"><span data-stu-id="69e9e-698">716 (0x2CC)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-699">% HS</span><span class="sxs-lookup"><span data-stu-id="69e9e-699">%hs</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERRO \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR\_WAS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-701">717 (0x2CD)</span><span class="sxs-lookup"><span data-stu-id="69e9e-701">717 (0x2CD)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-702">{Página bloqueada} Uma das páginas a serem bloqueadas já estava bloqueada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-702">{Page Locked} One of the pages to lock was already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**\_erro de \_ hardware do log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**ERROR\_LOG\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-704">718 (0x2CE)</span><span class="sxs-lookup"><span data-stu-id="69e9e-704">718 (0x2CE)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-705">Pop-up de aplicativo: %1: %2</span><span class="sxs-lookup"><span data-stu-id="69e9e-705">Application popup: %1 : %2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERRO \_ já \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="69e9e-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR\_ALREADY\_WIN32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-707">719 (0x2CF)</span><span class="sxs-lookup"><span data-stu-id="69e9e-707">719 (0x2CF)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-708">ERRO \_ já \_ Win32</span><span class="sxs-lookup"><span data-stu-id="69e9e-708">ERROR\_ALREADY\_WIN32</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**tipo de máquina de imagem de erro de não \_ \_ \_ \_ correspondência \_ exe**</span><span class="sxs-lookup"><span data-stu-id="69e9e-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-710">720 (0x2D0)</span><span class="sxs-lookup"><span data-stu-id="69e9e-710">720 (0x2D0)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-711">{Tipo de computador não compatível} O arquivo de imagem% HS é válido, mas é para um tipo de computador diferente do computador atual.</span><span class="sxs-lookup"><span data-stu-id="69e9e-711">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERRO \_ sem \_ rendimento \_ realizado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR\_NO\_YIELD\_PERFORMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-713">721 (0x2D1)</span><span class="sxs-lookup"><span data-stu-id="69e9e-713">721 (0x2D1)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-714">Uma execução de yield foi executada e nenhum thread estava disponível para execução.</span><span class="sxs-lookup"><span data-stu-id="69e9e-714">A yield execution was performed and no thread was available to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**retomada do timer de erro \_ \_ \_ ignorada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**ERROR\_TIMER\_RESUME\_IGNORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-716">722 (0x2D2)</span><span class="sxs-lookup"><span data-stu-id="69e9e-716">722 (0x2D2)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-717">O sinalizador retomável para uma API de timer foi ignorado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-717">The resumable flag to a timer API was ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERRO de \_ arbitragem \_ sem tratamento**</span><span class="sxs-lookup"><span data-stu-id="69e9e-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERROR\_ARBITRATION\_UNHANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-719">723 (0x2D3)</span><span class="sxs-lookup"><span data-stu-id="69e9e-719">723 (0x2D3)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-720">O arbitrador tem deferida a arbitragem desses recursos para seu pai.</span><span class="sxs-lookup"><span data-stu-id="69e9e-720">The arbiter has deferred arbitration of these resources to its parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERRO \_ CardBus \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="69e9e-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR\_CARDBUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-722">724 (0x2D4)</span><span class="sxs-lookup"><span data-stu-id="69e9e-722">724 (0x2D4)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-723">O dispositivo CardBus inserido não pode ser iniciado devido a um erro de configuração em "% hs".</span><span class="sxs-lookup"><span data-stu-id="69e9e-723">The inserted CardBus device cannot be started because of a configuration error on "%hs".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERRO \_ MP \_ \_ incompatível do processador**</span><span class="sxs-lookup"><span data-stu-id="69e9e-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR\_MP\_PROCESSOR\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-725">725 (0x2D5)</span><span class="sxs-lookup"><span data-stu-id="69e9e-725">725 (0x2D5)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-726">As CPUs nesse sistema multiprocessador não são do mesmo nível de revisão.</span><span class="sxs-lookup"><span data-stu-id="69e9e-726">The CPUs in this multiprocessor system are not all the same revision level.</span></span> <span data-ttu-id="69e9e-727">Para usar todos os processadores, o sistema operacional se restringe aos recursos do processador menos capaz no sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-727">To use all processors the operating system restricts itself to the features of the least capable processor in the system.</span></span> <span data-ttu-id="69e9e-728">Se ocorrerem problemas com este sistema, entre em contato com o fabricante da CPU para ver se há suporte para essa combinação de processadores.</span><span class="sxs-lookup"><span data-stu-id="69e9e-728">Should problems occur with this system, contact the CPU manufacturer to see if this mix of processors is supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERRO \_ hibernado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR\_HIBERNATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-730">726 (0x2D6)</span><span class="sxs-lookup"><span data-stu-id="69e9e-730">726 (0x2D6)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-731">O sistema foi colocado em hibernação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-731">The system was put into hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERRO \_ retomar \_ hibernação**</span><span class="sxs-lookup"><span data-stu-id="69e9e-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR\_RESUME\_HIBERNATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-733">727 (0x2D7)</span><span class="sxs-lookup"><span data-stu-id="69e9e-733">727 (0x2D7)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-734">O sistema foi retomado da hibernação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-734">The system was resumed from hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**FIRMWARE de erro \_ \_ atualizado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**ERROR\_FIRMWARE\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-736">728 (0x2D8)</span><span class="sxs-lookup"><span data-stu-id="69e9e-736">728 (0x2D8)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-737">O Windows detectou que o firmware do sistema (BIOS) foi atualizado na \[ data do firmware anterior = %2, data atual do firmware %3 \] .</span><span class="sxs-lookup"><span data-stu-id="69e9e-737">Windows has detected that the system firmware (BIOS) was updated \[previous firmware date = %2, current firmware date %3\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**DRIVERS de erro \_ \_ vazando \_ páginas bloqueadas \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERROR\_DRIVERS\_LEAKING\_LOCKED\_PAGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-739">729 (0x2D9)</span><span class="sxs-lookup"><span data-stu-id="69e9e-739">729 (0x2D9)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-740">Um driver de dispositivo está vazando páginas de e/s bloqueadas causando degradação do sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-740">A device driver is leaking locked I/O pages causing system degradation.</span></span> <span data-ttu-id="69e9e-741">O sistema habilitou automaticamente o código de rastreamento para tentar detectar o culpado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-741">The system has automatically enabled tracking code in order to try and catch the culprit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERRO \_ ao \_ sistema de ativação**</span><span class="sxs-lookup"><span data-stu-id="69e9e-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR\_WAKE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-743">730 (0x2DA)</span><span class="sxs-lookup"><span data-stu-id="69e9e-743">730 (0x2DA)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-744">O sistema tem acordado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-744">The system has awoken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERRO de \_ espera \_ 1**</span><span class="sxs-lookup"><span data-stu-id="69e9e-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR\_WAIT\_1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-746">731 (0x2DB)</span><span class="sxs-lookup"><span data-stu-id="69e9e-746">731 (0x2DB)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-747">ERRO de \_ espera \_ 1</span><span class="sxs-lookup"><span data-stu-id="69e9e-747">ERROR\_WAIT\_1</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERRO de \_ espera \_ 2**</span><span class="sxs-lookup"><span data-stu-id="69e9e-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERROR\_WAIT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-749">732 (0x2DC)</span><span class="sxs-lookup"><span data-stu-id="69e9e-749">732 (0x2DC)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-750">ERRO de \_ espera \_ 2</span><span class="sxs-lookup"><span data-stu-id="69e9e-750">ERROR\_WAIT\_2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERRO de \_ espera \_ 3**</span><span class="sxs-lookup"><span data-stu-id="69e9e-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR\_WAIT\_3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-752">733 (0x2DD)</span><span class="sxs-lookup"><span data-stu-id="69e9e-752">733 (0x2DD)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-753">ERRO de \_ espera \_ 3</span><span class="sxs-lookup"><span data-stu-id="69e9e-753">ERROR\_WAIT\_3</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERRO ao \_ aguardar \_ 63**</span><span class="sxs-lookup"><span data-stu-id="69e9e-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-755">734 (0x2DE)</span><span class="sxs-lookup"><span data-stu-id="69e9e-755">734 (0x2DE)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-756">ERRO ao \_ aguardar \_ 63</span><span class="sxs-lookup"><span data-stu-id="69e9e-756">ERROR\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERRO \_ abandonado- \_ aguardando \_ 0**</span><span class="sxs-lookup"><span data-stu-id="69e9e-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR\_ABANDONED\_WAIT\_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-758">735 (0x2DF)</span><span class="sxs-lookup"><span data-stu-id="69e9e-758">735 (0x2DF)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-759">ERRO \_ abandonado- \_ aguardando \_ 0</span><span class="sxs-lookup"><span data-stu-id="69e9e-759">ERROR\_ABANDONED\_WAIT\_0</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**Erro \_ abandonado ao \_ aguardar \_ 63**</span><span class="sxs-lookup"><span data-stu-id="69e9e-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR\_ABANDONED\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-761">736 (0x2E0)</span><span class="sxs-lookup"><span data-stu-id="69e9e-761">736 (0x2E0)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-762">Erro \_ abandonado ao \_ aguardar \_ 63</span><span class="sxs-lookup"><span data-stu-id="69e9e-762">ERROR\_ABANDONED\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERRO \_ de \_ APC do usuário**</span><span class="sxs-lookup"><span data-stu-id="69e9e-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR\_USER\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-764">737 (0x2E1)</span><span class="sxs-lookup"><span data-stu-id="69e9e-764">737 (0x2E1)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-765">ERRO \_ de \_ APC do usuário</span><span class="sxs-lookup"><span data-stu-id="69e9e-765">ERROR\_USER\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERRO do \_ kernel \_ APC**</span><span class="sxs-lookup"><span data-stu-id="69e9e-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR\_KERNEL\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-767">738 (0x2E2)</span><span class="sxs-lookup"><span data-stu-id="69e9e-767">738 (0x2E2)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-768">ERRO do \_ kernel \_ APC</span><span class="sxs-lookup"><span data-stu-id="69e9e-768">ERROR\_KERNEL\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERRO \_ alertado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR\_ALERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-770">739 (0x2E3)</span><span class="sxs-lookup"><span data-stu-id="69e9e-770">739 (0x2E3)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-771">ERRO \_ alertado</span><span class="sxs-lookup"><span data-stu-id="69e9e-771">ERROR\_ALERTED</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**elevação de erro \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="69e9e-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**ERROR\_ELEVATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-773">740 (0x2E4)</span><span class="sxs-lookup"><span data-stu-id="69e9e-773">740 (0x2E4)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-774">A operação solicitada requer elevação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-774">The requested operation requires elevation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERRO de \_ nova análise**</span><span class="sxs-lookup"><span data-stu-id="69e9e-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR\_REPARSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-776">741 (0x2E5)</span><span class="sxs-lookup"><span data-stu-id="69e9e-776">741 (0x2E5)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-777">Uma nova análise deve ser executada pelo Gerenciador de objetos, pois o nome do arquivo resultou em um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="69e9e-777">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERRO \_ \_ de bloqueio \_ de oplock em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="69e9e-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERROR\_OPLOCK\_BREAK\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-779">742 (0x2E6)</span><span class="sxs-lookup"><span data-stu-id="69e9e-779">742 (0x2E6)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-780">Uma operação abrir/criar foi concluída enquanto uma interrupção de oplock está em andamento.</span><span class="sxs-lookup"><span data-stu-id="69e9e-780">An open/create operation completed while an oplock break is underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**VOLUME de erro \_ \_ montado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**ERROR\_VOLUME\_MOUNTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-782">743 (0x2E7)</span><span class="sxs-lookup"><span data-stu-id="69e9e-782">743 (0x2E7)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-783">Um novo volume foi montado por um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-783">A new volume has been mounted by a file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERRO \_ RXACT \_ confirmado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR\_RXACT\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-785">744 (0x2E8)</span><span class="sxs-lookup"><span data-stu-id="69e9e-785">744 (0x2E8)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-786">Esse status de nível de êxito indica que o estado da transação já existe para a subárvore do registro, mas que uma confirmação de transação foi anulada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-786">This success level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="69e9e-787">A confirmação já foi concluída.</span><span class="sxs-lookup"><span data-stu-id="69e9e-787">The commit has now been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**\_aviso de notificação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR\_NOTIFY\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-789">745 (0x2E9)</span><span class="sxs-lookup"><span data-stu-id="69e9e-789">745 (0x2E9)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-790">Isso indica que uma solicitação notificar alteração foi concluída devido ao fechamento do identificador que fez a solicitação notificar alteração.</span><span class="sxs-lookup"><span data-stu-id="69e9e-790">This indicates that a notify change request has been completed due to closing the handle which made the notify change request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERRO \_ ao \_ conectar o transporte primário \_ \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="69e9e-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR\_PRIMARY\_TRANSPORT\_CONNECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-792">746 (0x2EA)</span><span class="sxs-lookup"><span data-stu-id="69e9e-792">746 (0x2EA)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-793">{Falha no Connect no transporte primário} Foi feita uma tentativa de conexão com o servidor remoto% hs no transporte primário, mas a conexão falhou.</span><span class="sxs-lookup"><span data-stu-id="69e9e-793">{Connect Failure on Primary Transport} An attempt was made to connect to the remote server %hs on the primary transport, but the connection failed.</span></span> <span data-ttu-id="69e9e-794">O computador foi capaz de se conectar em um transporte secundário.</span><span class="sxs-lookup"><span data-stu-id="69e9e-794">The computer WAS able to connect on a secondary transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_transição de \_ falha de página de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**ERROR\_PAGE\_FAULT\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-796">747 (0x2EB)</span><span class="sxs-lookup"><span data-stu-id="69e9e-796">747 (0x2EB)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-797">A falha de página era uma falha de transição.</span><span class="sxs-lookup"><span data-stu-id="69e9e-797">Page fault was a transition fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERRO \_ de \_ solicitação de falha de página \_ \_ zero**</span><span class="sxs-lookup"><span data-stu-id="69e9e-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERROR\_PAGE\_FAULT\_DEMAND\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-799">748 (0x2EC)</span><span class="sxs-lookup"><span data-stu-id="69e9e-799">748 (0x2EC)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-800">A falha de página era uma falha de demanda zero.</span><span class="sxs-lookup"><span data-stu-id="69e9e-800">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**\_ \_ falha \_ na cópia da página de erro \_ na \_ gravação**</span><span class="sxs-lookup"><span data-stu-id="69e9e-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR\_PAGE\_FAULT\_COPY\_ON\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-802">749 (0x2ED)</span><span class="sxs-lookup"><span data-stu-id="69e9e-802">749 (0x2ED)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-803">A falha de página era uma falha de demanda zero.</span><span class="sxs-lookup"><span data-stu-id="69e9e-803">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**\_página de \_ proteção de falha da página de \_ erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**ERROR\_PAGE\_FAULT\_GUARD\_PAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-805">750 (0x2EE)</span><span class="sxs-lookup"><span data-stu-id="69e9e-805">750 (0x2EE)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-806">A falha de página era uma falha de demanda zero.</span><span class="sxs-lookup"><span data-stu-id="69e9e-806">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_arquivo de \_ \_ paginação de falha de página de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**ERROR\_PAGE\_FAULT\_PAGING\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-808">751 (0x2EF)</span><span class="sxs-lookup"><span data-stu-id="69e9e-808">751 (0x2EF)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-809">A falha de página foi satisfeita pela leitura de um dispositivo de armazenamento secundário.</span><span class="sxs-lookup"><span data-stu-id="69e9e-809">Page fault was satisfied by reading from a secondary storage device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**página de cache de erro \_ \_ \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**ERROR\_CACHE\_PAGE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-811">752 (0x2F0)</span><span class="sxs-lookup"><span data-stu-id="69e9e-811">752 (0x2F0)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-812">A página armazenada em cache foi bloqueada durante a operação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-812">Cached page was locked during operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**\_despejo de falha de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERROR\_CRASH\_DUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-814">753 (0x2F1)</span><span class="sxs-lookup"><span data-stu-id="69e9e-814">753 (0x2F1)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-815">O despejo de memória existe no arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-815">Crash dump exists in paging file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**BUFFER de erros \_ \_ todos os \_ zeros**</span><span class="sxs-lookup"><span data-stu-id="69e9e-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**ERROR\_BUFFER\_ALL\_ZEROS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-817">754 (0x2F2)</span><span class="sxs-lookup"><span data-stu-id="69e9e-817">754 (0x2F2)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-818">O buffer especificado contém todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="69e9e-818">Specified buffer contains all zeros.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERRO ao \_ reanalisar \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="69e9e-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR\_REPARSE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-820">755 (0x2F3)</span><span class="sxs-lookup"><span data-stu-id="69e9e-820">755 (0x2F3)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-821">Uma nova análise deve ser executada pelo Gerenciador de objetos, pois o nome do arquivo resultou em um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="69e9e-821">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**requisitos de recursos de erro \_ \_ \_ alterados**</span><span class="sxs-lookup"><span data-stu-id="69e9e-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**ERROR\_RESOURCE\_REQUIREMENTS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-823">756 (0x2F4)</span><span class="sxs-lookup"><span data-stu-id="69e9e-823">756 (0x2F4)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-824">O dispositivo teve êxito em uma parada de consulta e seus requisitos de recursos foram alterados.</span><span class="sxs-lookup"><span data-stu-id="69e9e-824">The device has succeeded a query-stop and its resource requirements have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERRO de \_ conversão \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="69e9e-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERROR\_TRANSLATION\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-826">757 (0x2F5)</span><span class="sxs-lookup"><span data-stu-id="69e9e-826">757 (0x2F5)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-827">O tradutor converteu esses recursos no espaço global e nenhuma tradução adicional deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-827">The translator has translated these resources into the global space and no further translations should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERRO \_ nada \_ para \_ terminar**</span><span class="sxs-lookup"><span data-stu-id="69e9e-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERROR\_NOTHING\_TO\_TERMINATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-829">758 (0x2F6)</span><span class="sxs-lookup"><span data-stu-id="69e9e-829">758 (0x2F6)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-830">Um processo que está sendo encerrado não tem threads para encerrar.</span><span class="sxs-lookup"><span data-stu-id="69e9e-830">A process being terminated has no threads to terminate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**o \_ processo \_ de erro não está \_ no \_ trabalho**</span><span class="sxs-lookup"><span data-stu-id="69e9e-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**ERROR\_PROCESS\_NOT\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-832">759 (0x2F7)</span><span class="sxs-lookup"><span data-stu-id="69e9e-832">759 (0x2F7)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-833">O processo especificado não faz parte de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="69e9e-833">The specified process is not part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**\_processo \_ de erro no \_ trabalho**</span><span class="sxs-lookup"><span data-stu-id="69e9e-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR\_PROCESS\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-835">760 (0x2F8)</span><span class="sxs-lookup"><span data-stu-id="69e9e-835">760 (0x2F8)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-836">O processo especificado faz parte de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="69e9e-836">The specified process is part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERRO \_ de \_ hibernação de VOLSNAP \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="69e9e-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR\_VOLSNAP\_HIBERNATE\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-838">761 (0x2F9)</span><span class="sxs-lookup"><span data-stu-id="69e9e-838">761 (0x2F9)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-839">{Serviço de Cópias de Sombra de Volume} O sistema agora está pronto para hibernação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-839">{Volume Shadow Copy Service} The system is now ready for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERRO \_ FSFILTER \_ op \_ concluído \_ com êxito**</span><span class="sxs-lookup"><span data-stu-id="69e9e-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR\_FSFILTER\_OP\_COMPLETED\_SUCCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-841">762 (0x2FA)</span><span class="sxs-lookup"><span data-stu-id="69e9e-841">762 (0x2FA)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-842">Um sistema de arquivos ou driver de filtro do sistema de arquivos concluiu com êxito uma operação FsFilter.</span><span class="sxs-lookup"><span data-stu-id="69e9e-842">A file system or file system filter driver has successfully completed an FsFilter operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**vetor de interrupção de erro \_ \_ \_ já \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**ERROR\_INTERRUPT\_VECTOR\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-844">763 (0x2FB)</span><span class="sxs-lookup"><span data-stu-id="69e9e-844">763 (0x2FB)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-845">O vetor de interrupção especificado já estava conectado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-845">The specified interrupt vector was already connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**interrupção de erro \_ \_ ainda \_ conectada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERROR\_INTERRUPT\_STILL\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-847">764 (0x2FC)</span><span class="sxs-lookup"><span data-stu-id="69e9e-847">764 (0x2FC)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-848">O vetor de interrupção especificado ainda está conectado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-848">The specified interrupt vector is still connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERRO ao \_ aguardar \_ \_ oplock**</span><span class="sxs-lookup"><span data-stu-id="69e9e-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR\_WAIT\_FOR\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-850">765 (0x2FD)</span><span class="sxs-lookup"><span data-stu-id="69e9e-850">765 (0x2FD)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-851">Uma operação está bloqueada aguardando um oplock.</span><span class="sxs-lookup"><span data-stu-id="69e9e-851">An operation is blocked waiting for an oplock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERRO \_ de \_ tratamento da exceção DBG \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR\_DBG\_EXCEPTION\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-853">766 (0x2FE)</span><span class="sxs-lookup"><span data-stu-id="69e9e-853">766 (0x2FE)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-854">Exceção manipulada pelo depurador.</span><span class="sxs-lookup"><span data-stu-id="69e9e-854">Debugger handled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERRO \_ DBG \_ continuar**</span><span class="sxs-lookup"><span data-stu-id="69e9e-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR\_DBG\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-856">767 (0x2FF)</span><span class="sxs-lookup"><span data-stu-id="69e9e-856">767 (0x2FF)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-857">O depurador continuou.</span><span class="sxs-lookup"><span data-stu-id="69e9e-857">Debugger continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERRO \_ na \_ pilha pop de retorno de chamada \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERROR\_CALLBACK\_POP\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-859">768 (0x300)</span><span class="sxs-lookup"><span data-stu-id="69e9e-859">768 (0x300)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-860">Ocorreu uma exceção em um retorno de chamada de modo de usuário e o quadro de retorno de chamada do kernel deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="69e9e-860">An exception occurred in a user mode callback and the kernel callback frame should be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**\_compactação de erro \_ desabilitada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**ERROR\_COMPRESSION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-862">769 (0x301)</span><span class="sxs-lookup"><span data-stu-id="69e9e-862">769 (0x301)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-863">A compactação está desabilitada para este volume.</span><span class="sxs-lookup"><span data-stu-id="69e9e-863">Compression is disabled for this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERRO \_ CANTFETCHBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="69e9e-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR\_CANTFETCHBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-865">770 (0x302)</span><span class="sxs-lookup"><span data-stu-id="69e9e-865">770 (0x302)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-866">O provedor de dados não pode buscar versões anteriores por meio de um conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="69e9e-866">The data provider cannot fetch backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERRO \_ CANTSCROLLBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="69e9e-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR\_CANTSCROLLBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-868">771 (0x303)</span><span class="sxs-lookup"><span data-stu-id="69e9e-868">771 (0x303)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-869">O provedor de dados não pode rolar para trás por meio de um conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="69e9e-869">The data provider cannot scroll backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERRO \_ ROWSNOTRELEASED**</span><span class="sxs-lookup"><span data-stu-id="69e9e-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR\_ROWSNOTRELEASED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-871">772 (0x304)</span><span class="sxs-lookup"><span data-stu-id="69e9e-871">772 (0x304)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-872">O provedor de dados requer que os dados previamente buscados sejam liberados antes de solicitar mais dados.</span><span class="sxs-lookup"><span data-stu-id="69e9e-872">The data provider requires that previously fetched data is released before asking for more data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERRO \_ de \_ sinalizadores de assessor inválidos \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR\_BAD\_ACCESSOR\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-874">773 (0x305)</span><span class="sxs-lookup"><span data-stu-id="69e9e-874">773 (0x305)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-875">O provedor de dados não pôde interpretar os sinalizadores definidos para uma associação de coluna em um acessador.</span><span class="sxs-lookup"><span data-stu-id="69e9e-875">The data provider was not able to interpret the flags set for a column binding in an accessor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**erros de erro \_ \_ encontrados**</span><span class="sxs-lookup"><span data-stu-id="69e9e-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**ERROR\_ERRORS\_ENCOUNTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-877">774 (0x306)</span><span class="sxs-lookup"><span data-stu-id="69e9e-877">774 (0x306)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-878">Um ou mais erros ocorreram durante o processamento da solicitação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-878">One or more errors occurred while processing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERRO \_ não \_ compatível**</span><span class="sxs-lookup"><span data-stu-id="69e9e-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-880">775 (0x307)</span><span class="sxs-lookup"><span data-stu-id="69e9e-880">775 (0x307)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-881">A implementação não é capaz de executar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-881">The implementation is not capable of performing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**\_solicitação \_ de erro fora \_ de \_ sequência**</span><span class="sxs-lookup"><span data-stu-id="69e9e-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**ERROR\_REQUEST\_OUT\_OF\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-883">776 (0x308)</span><span class="sxs-lookup"><span data-stu-id="69e9e-883">776 (0x308)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-884">O cliente de um componente solicitou uma operação que não é válida, dado o estado da instância do componente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-884">The client of a component requested an operation which is not valid given the state of the component instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**\_erro de \_ análise da versão do erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**ERROR\_VERSION\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-886">777 (0x309)</span><span class="sxs-lookup"><span data-stu-id="69e9e-886">777 (0x309)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-887">Não foi possível analisar um número de versão.</span><span class="sxs-lookup"><span data-stu-id="69e9e-887">A version number could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERRO \_ BADSTARTPOSITION**</span><span class="sxs-lookup"><span data-stu-id="69e9e-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR\_BADSTARTPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-889">778 (0x30A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-889">778 (0x30A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-890">A posição inicial do iterador é inválida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-890">The iterator's start position is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**\_hardware de memória de erro \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERROR\_MEMORY\_HARDWARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-892">779 (0x30B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-892">779 (0x30B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-893">O hardware relatou um erro de memória não corrigível.</span><span class="sxs-lookup"><span data-stu-id="69e9e-893">The hardware has reported an uncorrectable memory error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**reparo do disco de erro \_ \_ \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR\_DISK\_REPAIR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-895">780 (0x30C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-895">780 (0x30C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-896">A operação tentada exigiu auto-recuperação para ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="69e9e-896">The attempted operation required self healing to be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERRO \_ \_ de recurso insuficiente \_ para o \_ \_ tamanho de seção compartilhada especificado \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR\_INSUFFICIENT\_RESOURCE\_FOR\_SPECIFIED\_SHARED\_SECTION\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-898">781 (0x30D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-898">781 (0x30D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-899">O heap de área de trabalho encontrou um erro ao alocar memória de sessão.</span><span class="sxs-lookup"><span data-stu-id="69e9e-899">The Desktop heap encountered an error while allocating session memory.</span></span> <span data-ttu-id="69e9e-900">Há mais informações no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="69e9e-900">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERRO \_ de \_ transição do PowerState do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-902">782 (0x30E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-902">782 (0x30E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-903">O estado de energia do sistema está em transição de %2 para %3.</span><span class="sxs-lookup"><span data-stu-id="69e9e-903">The system power state is transitioning from %2 to %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERRO \_ de \_ \_ transição complexa do PowerState do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_COMPLEX\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-905">783 (0x30F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-905">783 (0x30F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-906">O estado de energia do sistema está em transição de %2 para %3, mas pode inserir %4.</span><span class="sxs-lookup"><span data-stu-id="69e9e-906">The system power state is transitioning from %2 to %3 but could enter %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERRO \_ de \_ exceção de MCA**</span><span class="sxs-lookup"><span data-stu-id="69e9e-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR\_MCA\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-908">784 (0x310)</span><span class="sxs-lookup"><span data-stu-id="69e9e-908">784 (0x310)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-909">Um thread está sendo expedido com exceção de MCA devido ao MCA.</span><span class="sxs-lookup"><span data-stu-id="69e9e-909">A thread is getting dispatched with MCA EXCEPTION because of MCA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERRO \_ \_ de auditoria \_ de acesso por \_ política**</span><span class="sxs-lookup"><span data-stu-id="69e9e-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR\_ACCESS\_AUDIT\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-911">785 (0x311)</span><span class="sxs-lookup"><span data-stu-id="69e9e-911">785 (0x311)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-912">O acesso a %1 é monitorado pela regra de política %2.</span><span class="sxs-lookup"><span data-stu-id="69e9e-912">Access to %1 is monitored by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERRO \_ \_ de acesso desabilitado \_ não é uma \_ \_ interface do usuário mais segura \_ por \_ política**</span><span class="sxs-lookup"><span data-stu-id="69e9e-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_NO\_SAFER\_UI\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-914">786 (0x312)</span><span class="sxs-lookup"><span data-stu-id="69e9e-914">786 (0x312)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-915">O acesso a %1 foi restringido pelo administrador pela regra de política %2.</span><span class="sxs-lookup"><span data-stu-id="69e9e-915">Access to %1 has been restricted by your Administrator by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERRO \_ abandonar \_ HIBERFILE**</span><span class="sxs-lookup"><span data-stu-id="69e9e-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR\_ABANDON\_HIBERFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-917">787 (0x313)</span><span class="sxs-lookup"><span data-stu-id="69e9e-917">787 (0x313)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-918">Um arquivo de hibernação válido foi invalidado e deve ser abandonado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-918">A valid hibernation file has been invalidated and should be abandoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERRO \_ perdido \_ a \_ rede de dados WRITEBEHIND \_ \_ desconectada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-920">788 (0x314)</span><span class="sxs-lookup"><span data-stu-id="69e9e-920">788 (0x314)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-921">{Falha na gravação atrasada} O Windows não pôde salvar todos os dados para o arquivo% HS; os dados foram perdidos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-921">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="69e9e-922">Esse erro pode ser causado por problemas de conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="69e9e-922">This error may be caused by network connectivity issues.</span></span> <span data-ttu-id="69e9e-923">Tente salvar este arquivo em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="69e9e-923">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERRO \_ perdido \_ \_ \_ \_ erro do servidor de rede de dados WRITEBEHIND \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-925">789 (0x315)</span><span class="sxs-lookup"><span data-stu-id="69e9e-925">789 (0x315)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-926">{Falha na gravação atrasada} O Windows não pôde salvar todos os dados para o arquivo% HS; os dados foram perdidos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-926">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="69e9e-927">Esse erro foi retornado pelo servidor no qual o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="69e9e-927">This error was returned by the server on which the file exists.</span></span> <span data-ttu-id="69e9e-928">Tente salvar este arquivo em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="69e9e-928">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERRO \_ perdido \_ WRITEBEHIND \_ de \_ disco local de dados \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_LOCAL\_DISK\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-930">790 (0x316)</span><span class="sxs-lookup"><span data-stu-id="69e9e-930">790 (0x316)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-931">{Falha na gravação atrasada} O Windows não pôde salvar todos os dados para o arquivo% HS; os dados foram perdidos.</span><span class="sxs-lookup"><span data-stu-id="69e9e-931">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="69e9e-932">Esse erro pode ser causado se o dispositivo tiver sido removido ou se a mídia estiver protegida contra gravação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-932">This error may be caused if the device has been removed or the media is write-protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERRO \_ de \_ tabela MCFG inadequada \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR\_BAD\_MCFG\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-934">791 (0x317)</span><span class="sxs-lookup"><span data-stu-id="69e9e-934">791 (0x317)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-935">Os recursos necessários para este dispositivo estão em conflito com a tabela MCFG.</span><span class="sxs-lookup"><span data-stu-id="69e9e-935">The resources required for this device conflict with the MCFG table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERRO \_ de \_ reparo de disco \_ Redirecionado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR\_DISK\_REPAIR\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-937">792 (0x318)</span><span class="sxs-lookup"><span data-stu-id="69e9e-937">792 (0x318)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-938">Não foi possível executar o reparo de volume enquanto ele estiver online.</span><span class="sxs-lookup"><span data-stu-id="69e9e-938">The volume repair could not be performed while it is online.</span></span> <span data-ttu-id="69e9e-939">Agende para colocar o volume offline para que ele possa ser reparado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-939">Please schedule to take the volume offline so that it can be repaired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERRO \_ de \_ reparo de disco \_ malsucedido**</span><span class="sxs-lookup"><span data-stu-id="69e9e-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR\_DISK\_REPAIR\_UNSUCCESSFUL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-941">793 (0x319)</span><span class="sxs-lookup"><span data-stu-id="69e9e-941">793 (0x319)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-942">O reparo do volume não foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="69e9e-942">The volume repair was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERRO \_ de \_ log CORROMPIdo \_ cheio**</span><span class="sxs-lookup"><span data-stu-id="69e9e-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR\_CORRUPT\_LOG\_OVERFULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-944">794 (0x31A)</span><span class="sxs-lookup"><span data-stu-id="69e9e-944">794 (0x31A)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-945">Um dos logs de corrupção de volume está cheio.</span><span class="sxs-lookup"><span data-stu-id="69e9e-945">One of the volume corruption logs is full.</span></span> <span data-ttu-id="69e9e-946">Outras corrupções que podem ser detectadas não serão registradas em log.</span><span class="sxs-lookup"><span data-stu-id="69e9e-946">Further corruptions that may be detected won't be logged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERRO \_ de \_ log corrompido \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="69e9e-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR\_CORRUPT\_LOG\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-948">795 (0x31B)</span><span class="sxs-lookup"><span data-stu-id="69e9e-948">795 (0x31B)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-949">Um dos logs de corrupção de volume está internamente corrompido e precisa ser recriado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-949">One of the volume corruption logs is internally corrupted and needs to be recreated.</span></span> <span data-ttu-id="69e9e-950">O volume pode conter corrupções não detectadas e deve ser verificado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-950">The volume may contain undetected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERRO \_ de \_ log corrompido \_ indisponível**</span><span class="sxs-lookup"><span data-stu-id="69e9e-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR\_CORRUPT\_LOG\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-952">796 (0x31C)</span><span class="sxs-lookup"><span data-stu-id="69e9e-952">796 (0x31C)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-953">Um dos logs de corrupção de volume está indisponível para ser operado no.</span><span class="sxs-lookup"><span data-stu-id="69e9e-953">One of the volume corruption logs is unavailable for being operated on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERRO \_ log corrompido \_ \_ excluído \_ cheio**</span><span class="sxs-lookup"><span data-stu-id="69e9e-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR\_CORRUPT\_LOG\_DELETED\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-955">797 (0x31D)</span><span class="sxs-lookup"><span data-stu-id="69e9e-955">797 (0x31D)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-956">Um dos logs de corrupção de volume foi excluído enquanto ainda tem registros de corrupção neles.</span><span class="sxs-lookup"><span data-stu-id="69e9e-956">One of the volume corruption logs was deleted while still having corruption records in them.</span></span> <span data-ttu-id="69e9e-957">O volume contém danos detectados e deve ser verificado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-957">The volume contains detected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERRO \_ log corrompido \_ \_ limpo**</span><span class="sxs-lookup"><span data-stu-id="69e9e-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR\_CORRUPT\_LOG\_CLEARED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-959">798 (0x31E)</span><span class="sxs-lookup"><span data-stu-id="69e9e-959">798 (0x31E)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-960">Um dos logs de corrupção de volume foi limpo pelo Chkdsk e não contém mais danos reais.</span><span class="sxs-lookup"><span data-stu-id="69e9e-960">One of the volume corruption logs was cleared by chkdsk and no longer contains real corruptions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERRO \_ de \_ nome órfã \_ esgotado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR\_ORPHAN\_NAME\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-962">799 (0x31F)</span><span class="sxs-lookup"><span data-stu-id="69e9e-962">799 (0x31F)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-963">Existem arquivos órfãos no volume, mas não foi possível recuperá-los porque não foi possível criar mais nomes novos no diretório de recuperação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-963">Orphaned files exist on the volume but could not be recovered because no more new names could be created in the recovery directory.</span></span> <span data-ttu-id="69e9e-964">Os arquivos devem ser movidos do diretório de recuperação.</span><span class="sxs-lookup"><span data-stu-id="69e9e-964">Files must be moved from the recovery directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERRO \_ oplock \_ alternado \_ para o \_ novo \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="69e9e-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR\_OPLOCK\_SWITCHED\_TO\_NEW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-966">800 (0x320)</span><span class="sxs-lookup"><span data-stu-id="69e9e-966">800 (0x320)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-967">O oplock que estava associado a esse identificador agora está associado a um identificador diferente.</span><span class="sxs-lookup"><span data-stu-id="69e9e-967">The oplock that was associated with this handle is now associated with a different handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERRO \_ não é possível \_ conceder o \_ \_ oplock solicitado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR\_CANNOT\_GRANT\_REQUESTED\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-969">801 (0x321)</span><span class="sxs-lookup"><span data-stu-id="69e9e-969">801 (0x321)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-970">Não é possível conceder um oplock do nível solicitado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-970">An oplock of the requested level cannot be granted.</span></span> <span data-ttu-id="69e9e-971">Um oplock de um nível inferior pode estar disponível.</span><span class="sxs-lookup"><span data-stu-id="69e9e-971">An oplock of a lower level may be available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERRO \_ não é possível \_ interromper o \_ oplock**</span><span class="sxs-lookup"><span data-stu-id="69e9e-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR\_CANNOT\_BREAK\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-973">802 (0x322)</span><span class="sxs-lookup"><span data-stu-id="69e9e-973">802 (0x322)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-974">A operação não foi concluída com êxito porque isso causaria a interrupção de um oplock.</span><span class="sxs-lookup"><span data-stu-id="69e9e-974">The operation did not complete successfully because it would cause an oplock to be broken.</span></span> <span data-ttu-id="69e9e-975">O chamador solicitou que oplocks existentes não sejam quebrados.</span><span class="sxs-lookup"><span data-stu-id="69e9e-975">The caller has requested that existing oplocks not be broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**identificador de oplock de erro \_ \_ \_ fechado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERROR\_OPLOCK\_HANDLE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-977">803 (0x323)</span><span class="sxs-lookup"><span data-stu-id="69e9e-977">803 (0x323)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-978">O identificador ao qual este oplock estava associado foi fechado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-978">The handle with which this oplock was associated has been closed.</span></span> <span data-ttu-id="69e9e-979">O oplock agora está danificado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-979">The oplock is now broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERRO \_ sem \_ condição de Ace \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR\_NO\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-981">804 (0x324)</span><span class="sxs-lookup"><span data-stu-id="69e9e-981">804 (0x324)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-982">A entrada de controle de acesso (ACE) especificada não contém uma condição.</span><span class="sxs-lookup"><span data-stu-id="69e9e-982">The specified access control entry (ACE) does not contain a condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERRO \_ de \_ condição Ace inválida \_**</span><span class="sxs-lookup"><span data-stu-id="69e9e-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR\_INVALID\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-984">805 (0x325)</span><span class="sxs-lookup"><span data-stu-id="69e9e-984">805 (0x325)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-985">A entrada de controle de acesso (ACE) especificada contém uma condição inválida.</span><span class="sxs-lookup"><span data-stu-id="69e9e-985">The specified access control entry (ACE) contains an invalid condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**identificador de arquivo de erro \_ \_ \_ revogado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**ERROR\_FILE\_HANDLE\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-987">806 (0x326)</span><span class="sxs-lookup"><span data-stu-id="69e9e-987">806 (0x326)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-988">O acesso ao identificador de arquivo especificado foi revogado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-988">Access to the specified file handle has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_imagem \_ de erro em uma \_ \_ base diferente**</span><span class="sxs-lookup"><span data-stu-id="69e9e-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**ERROR\_IMAGE\_AT\_DIFFERENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-990">807 (0x327)</span><span class="sxs-lookup"><span data-stu-id="69e9e-990">807 (0x327)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-991">Um arquivo de imagem foi mapeado em um endereço diferente daquele especificado no arquivo de imagem, mas as correções ainda serão executadas automaticamente na imagem.</span><span class="sxs-lookup"><span data-stu-id="69e9e-991">An image file was mapped at a different address from the one specified in the image file but fixups will still be automatically performed on the image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERRO \_ de \_ acesso de ea \_ negado**</span><span class="sxs-lookup"><span data-stu-id="69e9e-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR\_EA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-993">994 (0x3E2)</span><span class="sxs-lookup"><span data-stu-id="69e9e-993">994 (0x3E2)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-994">O acesso ao atributo estendido foi negado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-994">Access to the extended attribute was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**operação de erro \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="69e9e-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERROR\_OPERATION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-996">995 (0x3E3)</span><span class="sxs-lookup"><span data-stu-id="69e9e-996">995 (0x3E3)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-997">A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69e9e-997">The I/O operation has been aborted because of either a thread exit or an application request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**\_e/s de erro \_ incompleta**</span><span class="sxs-lookup"><span data-stu-id="69e9e-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERROR\_IO\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-999">996 (0x3E4)</span><span class="sxs-lookup"><span data-stu-id="69e9e-999">996 (0x3E4)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-1000">O evento de e/s sobreposto não está em um estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="69e9e-1000">Overlapped I/O event is not in a signaled state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**\_e/s de erro \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="69e9e-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERROR\_IO\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-1002">997 (0x3E5)</span><span class="sxs-lookup"><span data-stu-id="69e9e-1002">997 (0x3E5)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-1003">A operação de e/s sobreposta está em andamento.</span><span class="sxs-lookup"><span data-stu-id="69e9e-1003">Overlapped I/O operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERRO \_ NOaccess**</span><span class="sxs-lookup"><span data-stu-id="69e9e-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR\_NOACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-1005">998 (0x3E6)</span><span class="sxs-lookup"><span data-stu-id="69e9e-1005">998 (0x3E6)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-1006">Acesso inválido ao local da memória.</span><span class="sxs-lookup"><span data-stu-id="69e9e-1006">Invalid access to memory location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69e9e-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERRO \_ SWAPERROR**</span><span class="sxs-lookup"><span data-stu-id="69e9e-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR\_SWAPERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e9e-1008">999 (0x3E7)</span><span class="sxs-lookup"><span data-stu-id="69e9e-1008">999 (0x3E7)</span></span>
</dt> <dt>



<span data-ttu-id="69e9e-1009">Erro ao executar operação de inpágina.</span><span class="sxs-lookup"><span data-stu-id="69e9e-1009">Error performing inpage operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="69e9e-1010">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69e9e-1010">Requirements</span></span>



| <span data-ttu-id="69e9e-1011">Requisito</span><span class="sxs-lookup"><span data-stu-id="69e9e-1011">Requirement</span></span> | <span data-ttu-id="69e9e-1012">Valor</span><span class="sxs-lookup"><span data-stu-id="69e9e-1012">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69e9e-1013">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69e9e-1013">Minimum supported client</span></span><br/> | <span data-ttu-id="69e9e-1014">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="69e9e-1014">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="69e9e-1015">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69e9e-1015">Minimum supported server</span></span><br/> | <span data-ttu-id="69e9e-1016">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69e9e-1016">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69e9e-1017">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69e9e-1017">Header</span></span><br/>                   | <dl> <span data-ttu-id="69e9e-1018"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="69e9e-1018"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69e9e-1019">Confira também</span><span class="sxs-lookup"><span data-stu-id="69e9e-1019">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e9e-1020">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="69e9e-1020">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
