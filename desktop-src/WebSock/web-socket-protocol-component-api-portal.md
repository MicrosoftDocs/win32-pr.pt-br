---
title: API de componente de protocolo WebSocket
description: .
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24edd74fe87185db498e6309a7fda5fa091c7d60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084704"
---
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="54ac2-103">API de componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="54ac2-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="54ac2-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="54ac2-104">Purpose</span></span>

<span data-ttu-id="54ac2-105">A API do componente de protocolo WebSocket permite canais de comunicação assíncronas e bidirecionais sobre HTTP que funcionam entre intermediários de rede existentes.</span><span class="sxs-lookup"><span data-stu-id="54ac2-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="54ac2-106">Com a API de componente de protocolo WebSocket, um cliente usa HTTP para se comunicar com um servidor e ambos os lados alternam para usando o protocolo subjacente em que o HTTP foi colocado em camadas (como TCP ou SSL).</span><span class="sxs-lookup"><span data-stu-id="54ac2-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="54ac2-107">O objetivo é primeiro usar HTTP para atravessar os intermediários da rede e, em seguida, usar o canal TCP/SSL subjacente de ponta a ponta para comunicação de aplicativo bidirecional.</span><span class="sxs-lookup"><span data-stu-id="54ac2-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="54ac2-108">O protocolo WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] é definido na IETF, enquanto um W3CAPI de API JavaScript associado \[ [](https://dev.w3.org/html5/websockets/) \] é definido no W3C.</span><span class="sxs-lookup"><span data-stu-id="54ac2-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54ac2-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="54ac2-109">In this section</span></span>



| <span data-ttu-id="54ac2-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="54ac2-110">Topic</span></span>                                                                                                          | <span data-ttu-id="54ac2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="54ac2-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="54ac2-112">**Tipos de dados da API do componente de protocolo WebSocket**</span><span class="sxs-lookup"><span data-stu-id="54ac2-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="54ac2-113">A API do componente de protocolo WebSocket define esses tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="54ac2-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="54ac2-114">Enumerações de API de componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="54ac2-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="54ac2-115">A API do componente de protocolo WebSocket define essas enumerações.</span><span class="sxs-lookup"><span data-stu-id="54ac2-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="54ac2-116">Funções da API do componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="54ac2-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="54ac2-117">A API do componente de protocolo WebSocket define essas funções.</span><span class="sxs-lookup"><span data-stu-id="54ac2-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="54ac2-118">Estruturas de API de componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="54ac2-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="54ac2-119">A API do componente de protocolo WebSocket define essas estruturas.</span><span class="sxs-lookup"><span data-stu-id="54ac2-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="54ac2-120">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="54ac2-120">Developer audience</span></span>

<span data-ttu-id="54ac2-121">A API do componente de protocolo WebSocket foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="54ac2-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="54ac2-122">É necessário ter familiaridade com a rede HTTP e do Windows.</span><span class="sxs-lookup"><span data-stu-id="54ac2-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="54ac2-123">A maneira preferida de usar o protocolo WebSocket no Windows é por meio da API do Windows [http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) ou do [namespace Windows. Networking. Sockets](/uwp/api/Windows.Networking.Sockets).</span><span class="sxs-lookup"><span data-stu-id="54ac2-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="54ac2-124">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="54ac2-124">Run-time requirements</span></span>

<span data-ttu-id="54ac2-125">A API do componente de protocolo WebSocket requer o Windows 8 e versões posteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="54ac2-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="54ac2-126">As APIs podem ser vinculadas dinamicamente por meio de websocket.dll.</span><span class="sxs-lookup"><span data-stu-id="54ac2-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="54ac2-127">websocket.dll fornece suporte para cabeçalhos HTTP relacionados a Handshakes de cliente e de servidor, verifica os dados de handshake recebidos e analisa o fluxo de dados WebSocket.</span><span class="sxs-lookup"><span data-stu-id="54ac2-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="54ac2-128">Ele não trata nenhuma operação específica de HTTP (redirecionamento, autenticação, suporte a proxy) nem executa operações de e/s (envio ou recebimento de bytes de fluxo do WebSocket).</span><span class="sxs-lookup"><span data-stu-id="54ac2-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="54ac2-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54ac2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ac2-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="54ac2-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="54ac2-131">WinHTTP (serviços HTTP do Windows)</span><span class="sxs-lookup"><span data-stu-id="54ac2-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

