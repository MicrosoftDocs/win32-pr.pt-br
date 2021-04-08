---
description: Cancela uma operação de espera registrada emitida pela função RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Função UnregisterWaitEx (Threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828532"
---
# <a name="unregisterwaitex-function"></a><span data-ttu-id="a11b3-103">Função UnregisterWaitEx</span><span class="sxs-lookup"><span data-stu-id="a11b3-103">UnregisterWaitEx function</span></span>

<span data-ttu-id="a11b3-104">Cancela uma operação de espera registrada emitida pela função [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="a11b3-104">Cancels a registered wait operation issued by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a11b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a11b3-105">Syntax</span></span>


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a><span data-ttu-id="a11b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a11b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a11b3-107">*WaitHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a11b3-107">*WaitHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a11b3-108">O identificador de espera.</span><span class="sxs-lookup"><span data-stu-id="a11b3-108">The wait handle.</span></span> <span data-ttu-id="a11b3-109">Esse identificador é retornado pela função [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="a11b3-109">This handle is returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

</dd> <dt>

<span data-ttu-id="a11b3-110">*CompletionEvent* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a11b3-110">*CompletionEvent* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a11b3-111">Um identificador para o objeto de evento a ser sinalizado quando a operação de espera tiver sido cancelada.</span><span class="sxs-lookup"><span data-stu-id="a11b3-111">A handle to the event object to be signaled when the wait operation has been unregistered.</span></span> <span data-ttu-id="a11b3-112">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a11b3-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="a11b3-113">Se esse parâmetro for **um \_ \_ valor de identificador inválido**, a função aguardará que todas as funções de retorno de chamada sejam concluídas antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="a11b3-113">If this parameter is **INVALID\_HANDLE\_VALUE**, the function waits for all callback functions to complete before returning.</span></span>

<span data-ttu-id="a11b3-114">Se esse parâmetro for **nulo**, a função marcará o temporizador para exclusão e retornará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a11b3-114">If this parameter is **NULL**, the function marks the timer for deletion and returns immediately.</span></span> <span data-ttu-id="a11b3-115">No entanto, a maioria dos chamadores deve aguardar a conclusão da função de retorno de chamada para que possa executar qualquer limpeza necessária.</span><span class="sxs-lookup"><span data-stu-id="a11b3-115">However, most callers should wait for the callback function to complete so they can perform any needed cleanup.</span></span>

<span data-ttu-id="a11b3-116">Se o chamador fornecer esse evento e a função for bem-sucedida ou se a função falhar com **erro e \_ /s \_ pendente**, não feche o evento até que ele seja sinalizado.</span><span class="sxs-lookup"><span data-stu-id="a11b3-116">If the caller provides this event and the function succeeds or the function fails with **ERROR\_IO\_PENDING**, do not close the event until it is signaled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a11b3-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a11b3-117">Return value</span></span>

<span data-ttu-id="a11b3-118">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a11b3-118">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="a11b3-119">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="a11b3-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="a11b3-120">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a11b3-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a11b3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="a11b3-121">Remarks</span></span>

<span data-ttu-id="a11b3-122">Você não pode fazer uma chamada de bloqueio para o **UnregisterWaitEx** de dentro de uma função de retorno para a mesma operação de espera.</span><span class="sxs-lookup"><span data-stu-id="a11b3-122">You cannot make a blocking call to **UnregisterWaitEx** from within a callback function for the same wait operation.</span></span> <span data-ttu-id="a11b3-123">Caso contrário, o retorno de chamada estará aguardando sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="a11b3-123">Otherwise, the callback will be waiting for itself to finish.</span></span> <span data-ttu-id="a11b3-124">Em geral, uma chamada de bloqueio para **UnregisterWaitEx** cria uma dependência entre o thread atual e o retorno de chamada, portanto, para fazer uma chamada de cancelamento de registro em outra operação de espera, você deve garantir que as funções de retorno de chamada não dependem umas das outras e que a segunda operação de espera também não execute uma chamada de cancelamento de registro na primeira operação.</span><span class="sxs-lookup"><span data-stu-id="a11b3-124">In general, a blocking call to **UnregisterWaitEx** creates a dependency between the current thread and the callback, so to make a blocking unregister call on another wait operation, you must ensure that the callback functions do not depend on one another and that the second wait operation does not also perform a blocking unregister call on the first operation.</span></span>

<span data-ttu-id="a11b3-125">Tenha cuidado ao fazer uma chamada **UnregisterWaitEx** de bloqueio em um thread persistente.</span><span class="sxs-lookup"><span data-stu-id="a11b3-125">Be careful when making a blocking **UnregisterWaitEx** call on a persistent thread.</span></span> <span data-ttu-id="a11b3-126">Se a operação de espera que está sendo cancelada pelo registro foi criada com **WT \_ EXECUTEINPERSISTENTTHREAD**, pode ocorrer um deadlock.</span><span class="sxs-lookup"><span data-stu-id="a11b3-126">If the wait operation being unregistered was created with **WT\_EXECUTEINPERSISTENTTHREAD**, a deadlock may occur.</span></span>

<span data-ttu-id="a11b3-127">Depois de fazer uma chamada de não bloqueio para **UnregisterWaitEx**, nenhuma nova função de retorno de chamada associada a *WaitHandle* pode ser enfileirada.</span><span class="sxs-lookup"><span data-stu-id="a11b3-127">After making non-blocking call to **UnregisterWaitEx**, no new callback functions associated with *WaitHandle* can be queued.</span></span> <span data-ttu-id="a11b3-128">No entanto, pode haver funções pendentes de retorno de chamada já enfileiradas para threads de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a11b3-128">However, there may be pending callback functions already queued to worker threads.</span></span>

<span data-ttu-id="a11b3-129">Em algumas condições, a função falhará com o **erro \_ e/s \_ pendente** se *CompletionEvent* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a11b3-129">Under some conditions, the function will fail with **ERROR\_IO\_PENDING** if *CompletionEvent* is **NULL**.</span></span> <span data-ttu-id="a11b3-130">Isso indica que há funções de retorno de chamada pendentes.</span><span class="sxs-lookup"><span data-stu-id="a11b3-130">This indicates that there are outstanding callback functions.</span></span> <span data-ttu-id="a11b3-131">Esses retornos de chamada serão executados ou estarão no meio da execução.</span><span class="sxs-lookup"><span data-stu-id="a11b3-131">Those callbacks either will execute or are in the middle of executing.</span></span>

<span data-ttu-id="a11b3-132">Se *CompletionEvent* for um identificador para um evento fornecido pelo chamador, é possível que a função seja bem-sucedida, falhe com **erro \_ e/s \_ pendente** ou falhe com um código de erro diferente.</span><span class="sxs-lookup"><span data-stu-id="a11b3-132">If *CompletionEvent* is a handle to an event provided by the caller, it is possible for the function to succeed, fail with **ERROR\_IO\_PENDING**, or fail with a different error code.</span></span> <span data-ttu-id="a11b3-133">Se a função for bem-sucedida ou se a função falhar com **erro \_ e/s \_ pendente**, o chamador sempre deverá esperar até que o evento seja sinalizado para fechar o evento.</span><span class="sxs-lookup"><span data-stu-id="a11b3-133">If the function succeeds, or if the function fails with **ERROR\_IO\_PENDING**, the caller should always wait until the event is signaled to close the event.</span></span> <span data-ttu-id="a11b3-134">Se a função falhar com um código de erro diferente, não será necessário aguardar até que o evento seja sinalizado para fechar o evento.</span><span class="sxs-lookup"><span data-stu-id="a11b3-134">If the function fails with a different error code, it is not necessary to wait until the event is signaled to close the event.</span></span>

<span data-ttu-id="a11b3-135">**Windows XP:** Se *CompletionEvent* for um identificador para um evento fornecido pelo chamador e a função falhar com **erro e \_ /s \_ pendente**, o chamador deverá aguardar até que o evento seja sinalizado para fechar o evento.</span><span class="sxs-lookup"><span data-stu-id="a11b3-135">**Windows XP:** If *CompletionEvent* is a handle to an event provided by the caller and the function fails with **ERROR\_IO\_PENDING**, the caller should wait until the event is signaled to close the event.</span></span> <span data-ttu-id="a11b3-136">Esse comportamento mudou a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a11b3-136">This behavior changed starting with Windows Vista.</span></span>

<span data-ttu-id="a11b3-137">Para compilar um aplicativo que usa essa função, defina **\_ Win32 \_ WinNT** como 0x0500 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a11b3-137">To compile an application that uses this function, define **\_WIN32\_WINNT** as 0x0500 or later.</span></span> <span data-ttu-id="a11b3-138">Para obter mais informações, consulte [usando os cabeçalhos do Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="a11b3-138">For more information, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a11b3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a11b3-139">Requirements</span></span>



| <span data-ttu-id="a11b3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a11b3-140">Requirement</span></span> | <span data-ttu-id="a11b3-141">Valor</span><span class="sxs-lookup"><span data-stu-id="a11b3-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a11b3-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a11b3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a11b3-143">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a11b3-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a11b3-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a11b3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a11b3-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a11b3-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a11b3-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a11b3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a11b3-147"><dt>Threadpoollegacyapiset. h no Windows 8 e no Windows Server 2012 (incluir Windows. h); </dt> <dt>Winbase. h no Windows 7, Windows server 2008 R2, Windows Vista, Windows Server 2008, Windows XP e Windows Server 2003 (inclua o Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a11b3-147"><dt>Threadpoollegacyapiset.h on Windows 8 and Windows Server 2012 (include Windows.h); </dt> <dt>WinBase.h on Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003 (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a11b3-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a11b3-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="a11b3-149"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a11b3-149"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a11b3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a11b3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a11b3-151"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a11b3-151"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a><span data-ttu-id="a11b3-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="a11b3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11b3-153">**RegisterWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="a11b3-153">**RegisterWaitForSingleObject**</span></span>](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[<span data-ttu-id="a11b3-154">Funções de sincronização</span><span class="sxs-lookup"><span data-stu-id="a11b3-154">Synchronization Functions</span></span>](synchronization-functions.md)
</dt> <dt>

[<span data-ttu-id="a11b3-155">Pooling de Thread </span><span class="sxs-lookup"><span data-stu-id="a11b3-155">Thread Pooling</span></span>](../procthread/thread-pooling.md)
</dt> </dl>

 

 
