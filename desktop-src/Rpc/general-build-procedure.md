---
title: Procedimento de Build geral
description: Página de navegação para o processo de criação de um aplicativo cliente/servidor usando RPC (chamada de procedimento remoto).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005393"
---
# <a name="general-build-procedure"></a><span data-ttu-id="843d1-103">Procedimento de Build geral</span><span class="sxs-lookup"><span data-stu-id="843d1-103">General Build Procedure</span></span>

<span data-ttu-id="843d1-104">O processo para criar um aplicativo cliente/servidor usando o Microsoft RPC é:</span><span class="sxs-lookup"><span data-stu-id="843d1-104">The process for creating a client/server application using Microsoft RPC is:</span></span>

-   <span data-ttu-id="843d1-105">Desenvolva a interface.</span><span class="sxs-lookup"><span data-stu-id="843d1-105">Develop the interface.</span></span>
-   <span data-ttu-id="843d1-106">Desenvolva o servidor que implementa a interface.</span><span class="sxs-lookup"><span data-stu-id="843d1-106">Develop the server that implements the interface.</span></span>
-   <span data-ttu-id="843d1-107">Desenvolva o cliente que usa a interface.</span><span class="sxs-lookup"><span data-stu-id="843d1-107">Develop the client that uses the interface.</span></span>

<span data-ttu-id="843d1-108">A figura a seguir ilustra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="843d1-108">The following figure illustrates these steps.</span></span>

![processo para criar um aplicativo cliente-servidor usando o Microsoft RPC](images/appdev.png)

<span data-ttu-id="843d1-110">É viável e comum desenvolver aplicativos cliente e servidor simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="843d1-110">It is feasible and common to develop the client and server applications concurrently.</span></span> <span data-ttu-id="843d1-111">Como os programas cliente e servidor dependem da interface, no entanto, a interface entre eles deve ser desenvolvida antes que o cliente e o servidor sejam desenvolvidos, conforme mostrado no diagrama anterior.</span><span class="sxs-lookup"><span data-stu-id="843d1-111">Since both the client and server programs are dependent on the interface, however, the interface between them must be developed before the client and server are developed, as shown in the preceding diagram.</span></span>

<span data-ttu-id="843d1-112">Esta seção aborda as etapas necessárias para a criação de um aplicativo cliente/servidor com RPC.</span><span class="sxs-lookup"><span data-stu-id="843d1-112">This section discusses the steps required for building a client/server application with RPC.</span></span> <span data-ttu-id="843d1-113">As informações são apresentadas nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="843d1-113">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="843d1-114">Desenvolvendo a interface</span><span class="sxs-lookup"><span data-stu-id="843d1-114">Developing the Interface</span></span>](developing-the-interface.md)
-   [<span data-ttu-id="843d1-115">Desenvolvendo o servidor</span><span class="sxs-lookup"><span data-stu-id="843d1-115">Developing the Server</span></span>](developing-the-server.md)
-   [<span data-ttu-id="843d1-116">Desenvolvendo o cliente</span><span class="sxs-lookup"><span data-stu-id="843d1-116">Developing the Client</span></span>](developing-the-client.md)

 

 




