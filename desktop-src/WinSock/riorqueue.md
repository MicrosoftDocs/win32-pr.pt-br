---
description: Especifica um descritor de soquete usado pelas solicitações de envio e recebimento com as extensões de e/s registradas do Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296597"
---
# <a name="rio_rq"></a><span data-ttu-id="c49f6-103">RIO de \_ RQ</span><span class="sxs-lookup"><span data-stu-id="c49f6-103">RIO\_RQ</span></span>

<span data-ttu-id="c49f6-104">O **typedef \_ RQ de Rio** especifica um descritor de soquete usado pelas solicitações de envio e recebimento com as extensões de e/s registradas do Winsock.</span><span class="sxs-lookup"><span data-stu-id="c49f6-104">The **RIO\_RQ** typedef specifies a socket descriptor used by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

<span data-ttu-id="c49f6-105">**RIO de \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="c49f6-105">**RIO\_RQ**</span></span>
</dt> <dd>

<span data-ttu-id="c49f6-106">Um tipo de dados que especifica um descritor de soquete usado pelas solicitações de envio e recebimento.</span><span class="sxs-lookup"><span data-stu-id="c49f6-106">A data type that specifies a socket descriptor used by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c49f6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c49f6-107">Remarks</span></span>

<span data-ttu-id="c49f6-108">As extensões de e/s registradas no Winsock operam principalmente em um objeto **rio \_ RQ** em vez de um soquete.</span><span class="sxs-lookup"><span data-stu-id="c49f6-108">The Winsock registered I/O extensions operate primarily on a **RIO\_RQ** object rather than a socket.</span></span> <span data-ttu-id="c49f6-109">Um aplicativo obtém um **Rio de \_ RQ** para um soquete existente usando a função [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) .</span><span class="sxs-lookup"><span data-stu-id="c49f6-109">An application obtains a **RIO\_RQ** for an existing socket using the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function.</span></span> <span data-ttu-id="c49f6-110">O soquete de entrada deve ter sido criado chamando-se a função [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) com o sinalizador **WSA \_ sinalizador \_ Rio** definido no parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="c49f6-110">The input socket must have been created by calling the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function with the **WSA\_FLAG\_RIO** flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="c49f6-111">Depois de obter um objeto **Rio de \_ RQ** , o descritor de soquete subjacente permanece válido.</span><span class="sxs-lookup"><span data-stu-id="c49f6-111">After obtaining a **RIO\_RQ** object, the underlying socket descriptor remains valid.</span></span> <span data-ttu-id="c49f6-112">Um aplicativo pode continuar a usar o soquete subjacente para definir e consultar opções de soquete, emitir IOCTLs e, por fim, fechar o soquete.</span><span class="sxs-lookup"><span data-stu-id="c49f6-112">An application may continue to use the underlying socket to set and query socket options, issue IOCTLs and ultimately close the socket.</span></span>

> [!Note]  
> <span data-ttu-id="c49f6-113">Para fins de eficiência, o acesso às filas de conclusão (as estruturas do [**rio \_ CQ**](riocqueue.md) ) e as filas de solicitação (do **rio \_ RQ** ) não são protegidos por primitivos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c49f6-113">For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](riocqueue.md) structs) and request queues (**RIO\_RQ** structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="c49f6-114">Se você precisar acessar uma fila de conclusão ou de solicitação de vários threads, o acesso deve ser coordenado por uma seção crítica, bloqueio de gravação de leitor fino ou mecanismo semelhante.</span><span class="sxs-lookup"><span data-stu-id="c49f6-114">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="c49f6-115">Esse bloqueio não é necessário para o acesso por um único thread.</span><span class="sxs-lookup"><span data-stu-id="c49f6-115">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="c49f6-116">Threads diferentes podem acessar filas de solicitações/conclusão separadas sem bloqueios.</span><span class="sxs-lookup"><span data-stu-id="c49f6-116">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="c49f6-117">A necessidade de sincronização ocorre somente quando vários threads tentam acessar a mesma fila.</span><span class="sxs-lookup"><span data-stu-id="c49f6-117">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="c49f6-118">A sincronização também será necessária se vários threads emitirem o envio e receberem no mesmo soquete, pois as operações de envio e recebimento usam a fila de solicitações do soquete.</span><span class="sxs-lookup"><span data-stu-id="c49f6-118">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="c49f6-119">O [**typedef \_ RQ do Rio**](riocqueue.md) é definido no arquivo de cabeçalho *Mswsockdef. h* que é incluído automaticamente no arquivo de cabeçalho *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="c49f6-119">The [**RIO\_RQ**](riocqueue.md) typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="c49f6-120">O arquivo de cabeçalho *Mswsockdef. h* nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="c49f6-120">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="c49f6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c49f6-121">Requirements</span></span>



| <span data-ttu-id="c49f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c49f6-122">Requirement</span></span> | <span data-ttu-id="c49f6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c49f6-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c49f6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c49f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c49f6-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c49f6-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="c49f6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c49f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c49f6-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c49f6-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="c49f6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c49f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c49f6-129"><dt>Mswsockdef. h (incluir mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c49f6-129"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c49f6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c49f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49f6-131">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="c49f6-131">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="c49f6-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="c49f6-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="c49f6-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="c49f6-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="c49f6-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c49f6-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c49f6-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="c49f6-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="c49f6-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c49f6-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c49f6-137">**WSASocket**</span><span class="sxs-lookup"><span data-stu-id="c49f6-137">**WSASocket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
