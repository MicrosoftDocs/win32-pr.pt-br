---
description: Especifica um descritor de buffer registrado usado com as extensões de e/s registradas do Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010771"
---
# <a name="rio_bufferid"></a><span data-ttu-id="ef8e5-103">RIO \_ bufferid</span><span class="sxs-lookup"><span data-stu-id="ef8e5-103">RIO\_BUFFERID</span></span>

<span data-ttu-id="ef8e5-104">O **typedef \_ bufferid de Rio** especifica um descritor de buffer registrado usado com as extensões de e/s registradas do Winsock.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-104">The **RIO\_BUFFERID** typedef specifies a registered buffer descriptor used with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

<span data-ttu-id="ef8e5-105">**RIO \_ bufferid**</span><span class="sxs-lookup"><span data-stu-id="ef8e5-105">**RIO\_BUFFERID**</span></span>
</dt> <dd>

<span data-ttu-id="ef8e5-106">Um tipo de dados que especifica um descritor de buffer registrado usado com solicitações de envio e recebimento.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-106">A data type that specifies a registered buffer descriptor used with send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef8e5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef8e5-107">Remarks</span></span>

<span data-ttu-id="ef8e5-108">As extensões de e/s registradas no Winsock operam principalmente em buffers registrados usando objetos do **rio \_ bufferid** .</span><span class="sxs-lookup"><span data-stu-id="ef8e5-108">The Winsock registered I/O extensions operate primarily on registered buffers using **RIO\_BUFFERID** objects.</span></span> <span data-ttu-id="ef8e5-109">Um aplicativo obtém um **rio \_ bufferid** para um buffer existente usando a função [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ef8e5-109">An application obtains a **RIO\_BUFFERID** for an existing buffer using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function.</span></span> <span data-ttu-id="ef8e5-110">Um aplicativo pode liberar um registro usando a função [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .</span><span class="sxs-lookup"><span data-stu-id="ef8e5-110">An application can release a registration using the [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function.</span></span>

<span data-ttu-id="ef8e5-111">Quando um buffer existente é registrado como um objeto **Rio de \_ bufferid** usando a função [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , determinados recursos internos são alocados da memória física e o buffer de aplicativo existente será bloqueado na memória física.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-111">When an existing buffer is registered as a **RIO\_BUFFERID** object using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function, certain internal resources are allocated from physical memory, and the existing application buffer will be locked into physical memory.</span></span> <span data-ttu-id="ef8e5-112">A função [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) é chamada para cancelar o registro do buffer, liberar esses recursos internos e permitir que o buffer seja desbloqueado e liberado da memória física.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-112">The [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function is called to deregister the buffer, free these internal resources, and allow the buffer to be unlocked and released from physical memory.</span></span>

<span data-ttu-id="ef8e5-113">O registro repetido e o cancelamento de registro de buffers de aplicativo usando as extensões de e/s registradas pelo Winsock podem causar uma degradação significativa no desempenho.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-113">Repeated registration and deregistration of application buffers using the Winsock registered I/O extensions may cause significant performance degradation.</span></span> <span data-ttu-id="ef8e5-114">As abordagens de gerenciamento de buffer a seguir devem ser consideradas ao criar um aplicativo usando as extensões de e/s registradas pelo Winsock para minimizar o registro repetido e o cancelamento de registro de buffers de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="ef8e5-114">The following buffer management approaches should be considered when designing an application using the Winsock registered I/O extensions to minimize repeated registration and deregistration of application buffers:</span></span>

-   <span data-ttu-id="ef8e5-115">• Maximize a reutilização de buffers.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-115">• Maximize the reuse of buffers.</span></span>
-   <span data-ttu-id="ef8e5-116">• Manter um pool limitado de buffers registrados não utilizados para uso pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-116">• Maintain a limited pool of unused registered buffers for use by the application.</span></span>
-   <span data-ttu-id="ef8e5-117">• Manter um pool limitado de buffers registrados e executar cópias de buffer entre esses buffers registrados e outros buffers não registrados.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-117">• Maintain a limited pool of registered buffers and perform buffer copies between these registered buffers and other unregistered buffers.</span></span>

<span data-ttu-id="ef8e5-118">O **typedef \_ bufferid do Rio** é definido no arquivo de cabeçalho *Mswsockdef. h* , que é incluído automaticamente no arquivo de cabeçalho *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="ef8e5-118">The **RIO\_BUFFERID** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="ef8e5-119">O arquivo de cabeçalho *Mswsockdef. h* nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="ef8e5-119">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef8e5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef8e5-120">Requirements</span></span>



| <span data-ttu-id="ef8e5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef8e5-121">Requirement</span></span> | <span data-ttu-id="ef8e5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ef8e5-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8e5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef8e5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef8e5-124">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef8e5-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="ef8e5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef8e5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef8e5-126">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef8e5-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ef8e5-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef8e5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef8e5-128"><dt>Mswsockdef. h (incluir mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef8e5-128"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef8e5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef8e5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef8e5-130">**RIO de \_ buf**</span><span class="sxs-lookup"><span data-stu-id="ef8e5-130">**RIO\_BUF**</span></span>](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[<span data-ttu-id="ef8e5-131">**RIODeregisterBuffer**</span><span class="sxs-lookup"><span data-stu-id="ef8e5-131">**RIODeregisterBuffer**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[<span data-ttu-id="ef8e5-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="ef8e5-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="ef8e5-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="ef8e5-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="ef8e5-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef8e5-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ef8e5-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="ef8e5-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="ef8e5-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef8e5-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> </dl>

 

 
