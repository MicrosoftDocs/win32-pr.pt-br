---
description: Fornece eventos para o Microsoft Windows HTTP Services (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Interface IWinHttpRequestEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789728"
---
# <a name="iwinhttprequestevents-interface"></a><span data-ttu-id="eb6e3-103">Interface IWinHttpRequestEvents</span><span class="sxs-lookup"><span data-stu-id="eb6e3-103">IWinHttpRequestEvents interface</span></span>

<span data-ttu-id="eb6e3-104">A interface **IWinHttpRequestEvents** fornece eventos para [o Microsoft Windows http Services (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="eb6e3-104">The **IWinHttpRequestEvents** interface provides events for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span> <span data-ttu-id="eb6e3-105">Ele usa apenas métodos de evento.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-105">It uses only event methods.</span></span>

## <a name="members"></a><span data-ttu-id="eb6e3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="eb6e3-106">Members</span></span>

<span data-ttu-id="eb6e3-107">A interface **IWinHttpRequestEvents** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="eb6e3-107">The **IWinHttpRequestEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="eb6e3-108">**IWinHttpRequestEvents** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eb6e3-108">**IWinHttpRequestEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="eb6e3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="eb6e3-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eb6e3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="eb6e3-110">Methods</span></span>

<span data-ttu-id="eb6e3-111">A interface **IWinHttpRequestEvents** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-111">The **IWinHttpRequestEvents** interface has these methods.</span></span>



| <span data-ttu-id="eb6e3-112">Método</span><span class="sxs-lookup"><span data-stu-id="eb6e3-112">Method</span></span>                                                                           | <span data-ttu-id="eb6e3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb6e3-113">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="eb6e3-114">**OnError**</span><span class="sxs-lookup"><span data-stu-id="eb6e3-114">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="eb6e3-115">Ocorre quando há um erro em tempo de execução no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-115">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="eb6e3-116">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="eb6e3-116">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="eb6e3-117">Ocorre quando os dados estão disponíveis da resposta.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-117">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="eb6e3-118">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="eb6e3-118">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="eb6e3-119">Ocorre quando os dados da resposta são concluídos.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-119">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="eb6e3-120">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="eb6e3-120">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="eb6e3-121">Ocorre quando os dados de resposta começam a ser recebidos.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-121">Occurs when the response data starts to be received.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="eb6e3-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb6e3-122">Remarks</span></span>

<span data-ttu-id="eb6e3-123">O procedimento a seguir descreve como registrar-se para notificações.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-123">The following procedure describes how to register for notifications.</span></span>

1.  <span data-ttu-id="eb6e3-124">Obtenha uma interface [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) chamando **QueryInterface** em um objeto [**IWinHttpRequest**](iwinhttprequest-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6e3-124">Get an [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface by calling **QueryInterface** on an [**IWinHttpRequest**](iwinhttprequest-interface.md) object.</span></span>
2.  <span data-ttu-id="eb6e3-125">Chame [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) na interface retornada e passe **\_ IWinHttpRequestEvents de IID** para *riid*.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-125">Call [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) on the returned interface and pass **IID\_IWinHttpRequestEvents** to *riid*.</span></span>
3.  <span data-ttu-id="eb6e3-126">Chame [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) no ponto de conexão retornado e passe um ponteiro para uma interface **IUnknown** em um objeto que implementa **IWinHttpRequestEvents** para *punk*.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-126">Call [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) on the returned connection point and pass a pointer to an **IUnknown** interface on an object that implements **IWinHttpRequestEvents** to *pUnk*.</span></span>

<span data-ttu-id="eb6e3-127">As notificações podem ser encerradas chamando [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) no ponto de conexão retornado na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-127">Notifications can be terminated by calling [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) on the connection point returned in step 2.</span></span>

<span data-ttu-id="eb6e3-128">Para exibir algum código que se registra para notificações COM, consulte a seção cliente do artigo [pontos de conexão com](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .</span><span class="sxs-lookup"><span data-stu-id="eb6e3-128">To view some code that registers for COM notifications, see the Client section of the [COM Connection Points](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) article.</span></span>

> [!Note]  
> <span data-ttu-id="eb6e3-129">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-129">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb6e3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb6e3-130">Requirements</span></span>



| <span data-ttu-id="eb6e3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb6e3-131">Requirement</span></span> | <span data-ttu-id="eb6e3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="eb6e3-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb6e3-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb6e3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="eb6e3-134">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="eb6e3-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="eb6e3-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb6e3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="eb6e3-136">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="eb6e3-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="eb6e3-137">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="eb6e3-137">Redistributable</span></span><br/>          | <span data-ttu-id="eb6e3-138">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="eb6e3-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="eb6e3-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="eb6e3-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb6e3-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb6e3-140"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb6e3-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb6e3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb6e3-142">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="eb6e3-142">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="eb6e3-143">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="eb6e3-143">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

