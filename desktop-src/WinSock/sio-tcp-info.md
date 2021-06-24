---
description: O código de controle recupera as estatísticas do protocolo TCP para um soquete especificado.
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: SIO_TCP_INFO código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f6076440f117ed287ad544c308e574454f33e2b7
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587795"
---
# <a name="sio_tcp_info-control-code"></a><span data-ttu-id="f4c3e-103">SIO_TCP_INFO código de controle</span><span class="sxs-lookup"><span data-stu-id="f4c3e-103">SIO_TCP_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="f4c3e-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4c3e-104">Description</span></span>

<span data-ttu-id="f4c3e-105">O código de controle de **\_ \_ informações TCP do sio** recupera as estatísticas do protocolo TCP para um soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-105">The **SIO\_TCP\_INFO** control code retrieves the Transmission Control Protocol (TCP) statistics for a specified socket.</span></span>

<span data-ttu-id="f4c3e-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="f4c3e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4c3e-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="f4c3e-108">s</span><span class="sxs-lookup"><span data-stu-id="f4c3e-108">s</span></span>

<span data-ttu-id="f4c3e-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-109">A descriptor that identifies a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="f4c3e-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="f4c3e-110">dwIoControlCode</span></span>

<span data-ttu-id="f4c3e-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-111">The control code for the operation.</span></span>
<span data-ttu-id="f4c3e-112">Use **as \_ \_ informações de TCP do sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-112">Use **SIO\_TCP\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="f4c3e-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="f4c3e-113">lpvInBuffer</span></span>

<span data-ttu-id="f4c3e-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="f4c3e-115">Esse parâmetro contém um ponteiro para um **DWORD** que especifica a versão do código de controle de **\_ \_ informações TCP sio** que você está usando.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-115">This parameter contains a pointer to a **DWORD** that specifies the version of the **SIO\_TCP\_INFO** control code that you are using.</span></span> <span data-ttu-id="f4c3e-116">Especifique 0 para usar [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span><span class="sxs-lookup"><span data-stu-id="f4c3e-116">Specify 0 to use [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span></span> <span data-ttu-id="f4c3e-117">Especifique 1 para usar [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), que fornece mais campos.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-117">Specify 1 to use [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), which provides more fields.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="f4c3e-118">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="f4c3e-118">cbInBuffer</span></span>

<span data-ttu-id="f4c3e-119">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-119">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="f4c3e-120">Esse parâmetro deve ser o tamanho do tipo de dados **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f4c3e-120">This parameter should be the size of the **DWORD** data type.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="f4c3e-121">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="f4c3e-121">lpvOutBuffer</span></span>

<span data-ttu-id="f4c3e-122">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-122">A pointer to the output buffer.</span></span>
<span data-ttu-id="f4c3e-123">Na saída bem-sucedida, esse parâmetro contém um ponteiro para uma estrutura de [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) que contém as estatísticas de TCP para o soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-123">On successful output, this parameter contains a pointer to a [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure that contains the TCP statistics for the specified socket.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="f4c3e-124">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="f4c3e-124">cbOutBuffer</span></span>

<span data-ttu-id="f4c3e-125">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-125">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="f4c3e-126">Esse parâmetro deve ter pelo menos o tamanho da estrutura de [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) .</span><span class="sxs-lookup"><span data-stu-id="f4c3e-126">This parameter must be at least the size of the [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="f4c3e-127">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="f4c3e-127">lpcbBytesReturned</span></span>

<span data-ttu-id="f4c3e-128">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-128">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="f4c3e-129">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-129">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="f4c3e-130">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-130">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="f4c3e-131">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-131">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="f4c3e-132">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-132">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="f4c3e-133">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-133">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="f4c3e-134">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="f4c3e-134">lpvOverlapped</span></span>

<span data-ttu-id="f4c3e-135">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="f4c3e-135">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="f4c3e-136">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-136">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="f4c3e-137">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="f4c3e-137">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="f4c3e-138">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-138">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="f4c3e-139">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-139">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="f4c3e-140">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-140">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="f4c3e-141">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="f4c3e-141">lpCompletionRoutine</span></span>

<span data-ttu-id="f4c3e-142">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="f4c3e-142">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="f4c3e-143">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="f4c3e-143">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="f4c3e-144">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="f4c3e-144">lpThreadId</span></span>

<span data-ttu-id="f4c3e-145">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="f4c3e-145">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="f4c3e-146">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-146">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="f4c3e-147">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="f4c3e-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="f4c3e-148">lpErrno</span><span class="sxs-lookup"><span data-stu-id="f4c3e-148">lpErrno</span></span>

<span data-ttu-id="f4c3e-149">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-149">A pointer to the error code.</span></span>

<span data-ttu-id="f4c3e-150">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="f4c3e-150">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4c3e-151">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f4c3e-151">Return value</span></span>

<span data-ttu-id="f4c3e-152">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-152">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="f4c3e-153">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-153">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="f4c3e-154">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="f4c3e-154">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="f4c3e-155">Código do erro</span><span class="sxs-lookup"><span data-stu-id="f4c3e-155">Error code</span></span> | <span data-ttu-id="f4c3e-156">Significado</span><span class="sxs-lookup"><span data-stu-id="f4c3e-156">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="f4c3e-157">**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-157">**WSAEMSGSIZE**</span></span> | <span data-ttu-id="f4c3e-158">O ponteiro para o buffer de entrada era **nulo** ou o tamanho especificado do buffer de entrada não estava correto.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-158">The pointer to the input buffer was **NULL**, or the specified size of the input buffer was not correct.</span></span> |
| <span data-ttu-id="f4c3e-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-159">**WSAEINVAL**</span></span> | <span data-ttu-id="f4c3e-160">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-160">An invalid argument was supplied.</span></span> <span data-ttu-id="f4c3e-161">Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-161">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |

## <a name="remarks"></a><span data-ttu-id="f4c3e-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4c3e-162">Remarks</span></span>

<span data-ttu-id="f4c3e-163">Ao contrário da recuperação de estatísticas TCP com a função [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) , a recuperação de estatísticas TCP com esse código de controle não exige que o código do usuário carregue, armazene e filtre a tabela de conexões TCP e não exija privilégios elevados para usar.</span><span class="sxs-lookup"><span data-stu-id="f4c3e-163">Unlike retrieving TCP statistics with the [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) function, retrieving TCP statistics with this control code does not require the user code to load, store, and filter the TCP connection table, and does not require elevated privileges to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4c3e-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4c3e-164">See also</span></span>

[<span data-ttu-id="f4c3e-165">SSA</span><span class="sxs-lookup"><span data-stu-id="f4c3e-165">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="f4c3e-166">**TCP_INFO_v0**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-166">**TCP_INFO_v0**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[<span data-ttu-id="f4c3e-167">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-167">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[<span data-ttu-id="f4c3e-168">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-168">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="f4c3e-169">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-169">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="f4c3e-170">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-170">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="f4c3e-171">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-171">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="f4c3e-172">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-172">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="f4c3e-173">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="f4c3e-173">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
