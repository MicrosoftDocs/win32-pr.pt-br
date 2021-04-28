---
title: API de componente de protocolo WebSocket
description: API de componente de protocolo WebSocket
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16290a7af5b5fea406e5f47c0db718d775e4d17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088814"
---
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="22f60-103">API de componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="22f60-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="22f60-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="22f60-104">Purpose</span></span>

<span data-ttu-id="22f60-105">A API do componente de protocolo WebSocket permite canais de comunicação assíncronas e bidirecionais sobre HTTP que funcionam entre intermediários de rede existentes.</span><span class="sxs-lookup"><span data-stu-id="22f60-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="22f60-106">Com a API de componente de protocolo WebSocket, um cliente usa HTTP para se comunicar com um servidor e ambos os lados alternam para usando o protocolo subjacente em que o HTTP foi colocado em camadas (como TCP ou SSL).</span><span class="sxs-lookup"><span data-stu-id="22f60-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="22f60-107">O objetivo é primeiro usar HTTP para atravessar os intermediários da rede e, em seguida, usar o canal TCP/SSL subjacente de ponta a ponta para comunicação de aplicativo bidirecional.</span><span class="sxs-lookup"><span data-stu-id="22f60-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="22f60-108">O protocolo WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] é definido na IETF, enquanto um W3CAPI de API JavaScript associado \[ [](https://dev.w3.org/html5/websockets/) \] é definido no W3C.</span><span class="sxs-lookup"><span data-stu-id="22f60-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22f60-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="22f60-109">In this section</span></span>



| <span data-ttu-id="22f60-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="22f60-110">Topic</span></span>                                                                                                          | <span data-ttu-id="22f60-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="22f60-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="22f60-112">**Tipos de dados da API do componente de protocolo WebSocket**</span><span class="sxs-lookup"><span data-stu-id="22f60-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="22f60-113">A API do componente de protocolo WebSocket define esses tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="22f60-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="22f60-114">Enumerações de API de componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="22f60-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="22f60-115">A API do componente de protocolo WebSocket define essas enumerações.</span><span class="sxs-lookup"><span data-stu-id="22f60-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="22f60-116">Funções da API do componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="22f60-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="22f60-117">A API do componente de protocolo WebSocket define essas funções.</span><span class="sxs-lookup"><span data-stu-id="22f60-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="22f60-118">Estruturas de API de componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="22f60-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="22f60-119">A API do componente de protocolo WebSocket define essas estruturas.</span><span class="sxs-lookup"><span data-stu-id="22f60-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="22f60-120">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="22f60-120">Developer audience</span></span>

<span data-ttu-id="22f60-121">A API do componente de protocolo WebSocket foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="22f60-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="22f60-122">É necessário ter familiaridade com a rede HTTP e do Windows.</span><span class="sxs-lookup"><span data-stu-id="22f60-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="22f60-123">A maneira preferida de usar o protocolo WebSocket no Windows é por meio da API do Windows [http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) ou do [namespace Windows. Networking. Sockets](/uwp/api/Windows.Networking.Sockets).</span><span class="sxs-lookup"><span data-stu-id="22f60-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="22f60-124">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="22f60-124">Run-time requirements</span></span>

<span data-ttu-id="22f60-125">A API do componente de protocolo WebSocket requer o Windows 8 e versões posteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="22f60-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="22f60-126">As APIs podem ser vinculadas dinamicamente por meio de websocket.dll.</span><span class="sxs-lookup"><span data-stu-id="22f60-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="22f60-127">websocket.dll fornece suporte para cabeçalhos HTTP relacionados a Handshakes de cliente e de servidor, verifica os dados de handshake recebidos e analisa o fluxo de dados WebSocket.</span><span class="sxs-lookup"><span data-stu-id="22f60-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="22f60-128">Ele não trata nenhuma operação específica de HTTP (redirecionamento, autenticação, suporte a proxy) nem executa operações de e/s (envio ou recebimento de bytes de fluxo do WebSocket).</span><span class="sxs-lookup"><span data-stu-id="22f60-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="22f60-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22f60-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22f60-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="22f60-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="22f60-131">WinHTTP (serviços HTTP do Windows)</span><span class="sxs-lookup"><span data-stu-id="22f60-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

