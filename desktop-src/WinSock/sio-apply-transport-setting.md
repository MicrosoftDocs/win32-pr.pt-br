---
description: O código de controle aplica uma ou mais configurações de transporte a um soquete.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: SIO_APPLY_TRANSPORT_SETTING código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105816040"
---
# <a name="sio_apply_transport_setting-control-code"></a><span data-ttu-id="6beaa-103">SIO_APPLY_TRANSPORT_SETTING código de controle</span><span class="sxs-lookup"><span data-stu-id="6beaa-103">SIO_APPLY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="6beaa-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="6beaa-104">Description</span></span>

<span data-ttu-id="6beaa-105">O código de controle de **\_ configuração de \_ transporte \_ sio Apply** aplica uma ou mais configurações de transporte a um soquete.</span><span class="sxs-lookup"><span data-stu-id="6beaa-105">The **SIO\_APPLY\_TRANSPORT\_SETTING** control code applies one or more transport settings to a socket.</span></span>

<span data-ttu-id="6beaa-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="6beaa-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="6beaa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6beaa-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="6beaa-108">s</span><span class="sxs-lookup"><span data-stu-id="6beaa-108">s</span></span>

<span data-ttu-id="6beaa-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="6beaa-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="6beaa-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="6beaa-110">dwIoControlCode</span></span>

<span data-ttu-id="6beaa-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="6beaa-111">The control code for the operation.</span></span>
<span data-ttu-id="6beaa-112">Use **a \_ \_ \_ configuração aplicar transporte do sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="6beaa-112">Use **SIO\_APPLY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="6beaa-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="6beaa-113">lpvInBuffer</span></span>

<span data-ttu-id="6beaa-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="6beaa-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="6beaa-115">Esse parâmetro contém um ponteiro para uma estrutura em que o primeiro membro da estrutura é uma estrutura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) que determina qual configuração de transporte está sendo aplicada.</span><span class="sxs-lookup"><span data-stu-id="6beaa-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being applied.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="6beaa-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="6beaa-116">cbInBuffer</span></span>

<span data-ttu-id="6beaa-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="6beaa-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="6beaa-118">Esse parâmetro depende da configuração de transporte que está sendo aplicada.</span><span class="sxs-lookup"><span data-stu-id="6beaa-118">This parameter depends on the transport setting being applied.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="6beaa-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="6beaa-119">lpvOutBuffer</span></span>

<span data-ttu-id="6beaa-120">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="6beaa-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="6beaa-121">Esse parâmetro depende da configuração de transporte que está sendo aplicada.</span><span class="sxs-lookup"><span data-stu-id="6beaa-121">This parameter depends on the transport setting being applied.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="6beaa-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="6beaa-122">cbOutBuffer</span></span>

<span data-ttu-id="6beaa-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="6beaa-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="6beaa-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="6beaa-124">lpcbBytesReturned</span></span>

<span data-ttu-id="6beaa-125">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="6beaa-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="6beaa-126">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="6beaa-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="6beaa-127">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="6beaa-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="6beaa-128">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="6beaa-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="6beaa-129">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6beaa-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="6beaa-130">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="6beaa-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="6beaa-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="6beaa-131">lpvOverlapped</span></span>

<span data-ttu-id="6beaa-132">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="6beaa-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="6beaa-133">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="6beaa-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="6beaa-134">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="6beaa-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="6beaa-135">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="6beaa-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="6beaa-136">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="6beaa-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="6beaa-137">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="6beaa-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="6beaa-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="6beaa-138">lpCompletionRoutine</span></span>

<span data-ttu-id="6beaa-139">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="6beaa-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="6beaa-140">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="6beaa-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="6beaa-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="6beaa-141">lpThreadId</span></span>

<span data-ttu-id="6beaa-142">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="6beaa-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="6beaa-143">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="6beaa-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="6beaa-144">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="6beaa-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="6beaa-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="6beaa-145">lpErrno</span></span>

<span data-ttu-id="6beaa-146">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="6beaa-146">A pointer to the error code.</span></span>

<span data-ttu-id="6beaa-147">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="6beaa-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="6beaa-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6beaa-148">Return value</span></span>

<span data-ttu-id="6beaa-149">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="6beaa-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="6beaa-150">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="6beaa-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="6beaa-151">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="6beaa-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="6beaa-152">Código do erro</span><span class="sxs-lookup"><span data-stu-id="6beaa-152">Error code</span></span> | <span data-ttu-id="6beaa-153">Significado</span><span class="sxs-lookup"><span data-stu-id="6beaa-153">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="6beaa-154">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="6beaa-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="6beaa-155">A operação de e/s sobreposta está em andamento.</span><span class="sxs-lookup"><span data-stu-id="6beaa-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="6beaa-156">Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="6beaa-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="6beaa-157">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="6beaa-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="6beaa-158">A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6beaa-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="6beaa-159">Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="6beaa-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="6beaa-160">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="6beaa-160">**WSAEFAULT**</span></span> | <span data-ttu-id="6beaa-161">O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="6beaa-161">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="6beaa-162">Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="6beaa-162">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="6beaa-163">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="6beaa-163">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="6beaa-164">Uma operação de bloqueio está atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="6beaa-164">A blocking operation is currently executing.</span></span> <span data-ttu-id="6beaa-165">Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="6beaa-165">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="6beaa-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="6beaa-166">**WSAEINTR**</span></span> | <span data-ttu-id="6beaa-167">Uma operação de bloqueio foi interrompida por uma chamada para [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="6beaa-167">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="6beaa-168">Esse erro será retornado se uma operação de bloqueio tiver sido interrompida.</span><span class="sxs-lookup"><span data-stu-id="6beaa-168">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="6beaa-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="6beaa-169">**WSAEINVAL**</span></span> | <span data-ttu-id="6beaa-170">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="6beaa-170">An invalid argument was supplied.</span></span> <span data-ttu-id="6beaa-171">Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="6beaa-171">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="6beaa-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="6beaa-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="6beaa-173">Uma operação de soquete encontrou uma rede inoperante.</span><span class="sxs-lookup"><span data-stu-id="6beaa-173">A socket operation encountered a dead network.</span></span> <span data-ttu-id="6beaa-174">Esse erro será retornado se o subsistema de rede tiver falhado.</span><span class="sxs-lookup"><span data-stu-id="6beaa-174">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="6beaa-175">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="6beaa-175">**WSAENOTSOCK**</span></span> | <span data-ttu-id="6beaa-176">Uma operação foi tentada em algo que não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="6beaa-176">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="6beaa-177">Esse erro será retornado se o descritor *s* não for um soquete.</span><span class="sxs-lookup"><span data-stu-id="6beaa-177">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="6beaa-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="6beaa-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="6beaa-179">Não há suporte para a operação tentada para o tipo de objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="6beaa-179">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="6beaa-180">Esse erro será retornado se o comando IOCTL especificado não tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="6beaa-180">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="6beaa-181">Esse erro também será retornado se a **\_ configuração de \_ transporte \_ sio aplicar** o IOCTL não tiver suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="6beaa-181">This error is also returned if the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="6beaa-182">Esse erro também é retornado quando uma tentativa de usar a **\_ configuração de \_ transporte \_ sio Apply** do IOCTL é feita em um soquete diferente de UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="6beaa-182">This error is also returned when an attempt to use the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="6beaa-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="6beaa-183">Remarks</span></span>

<span data-ttu-id="6beaa-184">O IOCTL de **\_ configuração de \_ transporte \_ sio Apply** tem suporte no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6beaa-184">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="6beaa-185">A **\_ configuração de \_ transporte \_ sio de aplicação** do IOCTL é um IOCTL genérico usado para aplicar a configuração de transporte ao soquete.</span><span class="sxs-lookup"><span data-stu-id="6beaa-185">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to apply transport setting to socket.</span></span>
<span data-ttu-id="6beaa-186">A configuração de transporte sendo aplicada é baseada no [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passado no parâmetro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="6beaa-186">The transport setting being applied is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="6beaa-187">A partir do Windows 8 e do Windows Server 2012, o sistema define o recurso de **REAL_TIME_NOTIFICATION_CAPABILITY** em um soquete TCP.</span><span class="sxs-lookup"><span data-stu-id="6beaa-187">Starting with Windows 8 and Windows Server 2012, the system defines the **REAL_TIME_NOTIFICATION_CAPABILITY** capability on a TCP socket.</span></span>
<span data-ttu-id="6beaa-188">A partir do Windows 10 e do Windows Server 2016, o **\_ \_ contexto NAMERES associado** também é definido.</span><span class="sxs-lookup"><span data-stu-id="6beaa-188">Starting with Windows 10 and Windows Server 2016, **ASSOCIATE\_NAMERES\_CONTEXT** is also defined.</span></span>
<span data-ttu-id="6beaa-189">Para obter mais informações, consulte [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) e [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span><span class="sxs-lookup"><span data-stu-id="6beaa-189">For more information, see [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span></span>

<span data-ttu-id="6beaa-190">Se o [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passado no parâmetro lpvInBuffer tiver o membro GUID definido como **recurso de \_ \_ notificação em \_ tempo real**, essa será uma solicitação para aplicar configurações de notificação em tempo real para o soquete TCP usado com o [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para receber notificações de rede em segundo plano em um aplicativo da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6beaa-190">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the lpvInBuffer parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to apply real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="6beaa-191">O parâmetro *lpvInBuffer* deve apontar para uma estrutura de **REAL_TIME_NOTIFICATION_SETTING_INPUT** .</span><span class="sxs-lookup"><span data-stu-id="6beaa-191">The *lpvInBuffer* parameter should point to a **REAL_TIME_NOTIFICATION_SETTING_INPUT** structure.</span></span>
<span data-ttu-id="6beaa-192">O parâmetro *lpvOutBuffer* não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="6beaa-192">The *lpvOutBuffer* parameter is unused for this operation.</span></span>
<span data-ttu-id="6beaa-193">Essa configuração de transporte aplica-se somente a soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="6beaa-193">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="6beaa-194">Essa configuração de transporte fornece uma maneira para que o WinInet ou serviços de rede semelhantes marquem um determinado soquete TCP como [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) habilitado.</span><span class="sxs-lookup"><span data-stu-id="6beaa-194">This transport setting provides a way for WinInet or similar network services to mark a given TCP socket as [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) enabled.</span></span>
<span data-ttu-id="6beaa-195">O Windows marcará o soquete TCP correspondente e definirá as configurações de hardware e software apropriadas quando essa opção for chamada.</span><span class="sxs-lookup"><span data-stu-id="6beaa-195">Windows will mark the corresponding TCP socket and configure appropriate hardware and software settings when this option is called.</span></span>
<span data-ttu-id="6beaa-196">Um aplicativo da Windows Store não chamará esse IOCTL diretamente.</span><span class="sxs-lookup"><span data-stu-id="6beaa-196">A Windows Store app will not call this IOCTL directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="6beaa-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="6beaa-197">See also</span></span>

[<span data-ttu-id="6beaa-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="6beaa-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="6beaa-199">SSA</span><span class="sxs-lookup"><span data-stu-id="6beaa-199">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="6beaa-200">**SIO_QUERY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="6beaa-200">**SIO_QUERY_TRANSPORT_SETTING**</span></span>](sio-query-transport-setting.md)

[<span data-ttu-id="6beaa-201">**TRANSPORT_SETTING_ID**</span><span class="sxs-lookup"><span data-stu-id="6beaa-201">**TRANSPORT_SETTING_ID**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[<span data-ttu-id="6beaa-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="6beaa-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="6beaa-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="6beaa-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="6beaa-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="6beaa-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="6beaa-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="6beaa-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="6beaa-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="6beaa-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="6beaa-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="6beaa-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
