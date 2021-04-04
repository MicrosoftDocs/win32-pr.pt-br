---
title: API do servidor HTTP
description: A API do servidor HTTP permite que os aplicativos se comuniquem via HTTP sem usar o Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API do servidor HTTP
- API do servidor HTTP, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084535"
---
# <a name="http-server-api"></a><span data-ttu-id="37fbb-105">API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="37fbb-105">HTTP Server API</span></span>

## <a name="purpose"></a><span data-ttu-id="37fbb-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="37fbb-106">Purpose</span></span>

<span data-ttu-id="37fbb-107">A API do servidor HTTP permite que os aplicativos se comuniquem via HTTP sem usar o Microsoft Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="37fbb-107">The HTTP Server API enables applications to communicate over HTTP without using Microsoft Internet Information Server (IIS).</span></span> <span data-ttu-id="37fbb-108">Os aplicativos podem se registrar para receber solicitações HTTP para URLs específicas, receber solicitações HTTP e enviar respostas HTTP.</span><span class="sxs-lookup"><span data-stu-id="37fbb-108">Applications can register to receive HTTP requests for particular URLs, receive HTTP requests, and send HTTP responses.</span></span> <span data-ttu-id="37fbb-109">A API do servidor HTTP inclui suporte a SSL para que os aplicativos possam trocar dados por conexões HTTP seguras sem o IIS.</span><span class="sxs-lookup"><span data-stu-id="37fbb-109">The HTTP Server API includes SSL support so that applications can exchange data over secure HTTP connections without IIS.</span></span> <span data-ttu-id="37fbb-110">Ele também foi projetado para funcionar com portas de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="37fbb-110">It is also designed to work with I/O completion ports.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="37fbb-111">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="37fbb-111">Developer audience</span></span>

<span data-ttu-id="37fbb-112">Essa API foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="37fbb-112">This API is designed for use by C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="37fbb-113">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="37fbb-113">Run-time requirements</span></span>

<span data-ttu-id="37fbb-114">A API do servidor HTTP tem suporte nos sistemas operacionais Windows Server 2003 e no Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="37fbb-114">The HTTP Server API is supported on Windows Server 2003 operating systems and on Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="37fbb-115">Lembre-se de que o Microsoft IIS 5 em execução no Windows XP com SP2 não é capaz de compartilhar a porta 80 com outros aplicativos HTTP em execução simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="37fbb-115">Be aware that Microsoft IIS 5 running on Windows XP with SP2 is not able to share port 80 with other HTTP applications running simultaneously.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37fbb-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="37fbb-116">In this section</span></span>



| <span data-ttu-id="37fbb-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="37fbb-117">Topic</span></span>                                                                           | <span data-ttu-id="37fbb-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="37fbb-118">Description</span></span>                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37fbb-119">Sobre a API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="37fbb-119">About HTTP Server API</span></span>](about-http-server-api.md)<br/>                   | <span data-ttu-id="37fbb-120">Informações gerais sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="37fbb-120">General information about HTTP.</span></span><br/>                                                              |
| [<span data-ttu-id="37fbb-121">Usando a API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="37fbb-121">Using HTTP Server API</span></span>](using-http-server-api.md)<br/>                   | <span data-ttu-id="37fbb-122">Guia de procedimentos para usar HTTP.</span><span class="sxs-lookup"><span data-stu-id="37fbb-122">Procedural guide for using HTTP.</span></span><br/>                                                             |
| [<span data-ttu-id="37fbb-123">Referência de API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="37fbb-123">HTTP Server API Reference</span></span>](http-server-api-reference.md)<br/>           | <span data-ttu-id="37fbb-124">Documentação de funções específicas, estruturas e tipos de enumeração disponíveis em HTTP.</span><span class="sxs-lookup"><span data-stu-id="37fbb-124">Documentation of specific functions, structures, and enumeration types available in HTTP.</span></span><br/>    |
| [<span data-ttu-id="37fbb-125">Aplicativo de exemplo do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="37fbb-125">HTTP Server Sample Application</span></span>](http-server-sample-application.md)<br/> | <span data-ttu-id="37fbb-126">Um aplicativo de exemplo que mostra como usar a API do servidor HTTP para executar tarefas do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="37fbb-126">A sample application that shows how to use the HTTP Server API to perform server-side tasks.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="37fbb-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37fbb-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37fbb-128">WinHTTP (serviços HTTP do Windows)</span><span class="sxs-lookup"><span data-stu-id="37fbb-128">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

