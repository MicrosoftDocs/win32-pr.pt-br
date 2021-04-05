---
description: A arquitetura do Windows Sockets 2 (Winsock) é compatível com a arquitetura do sistema aberto do Windows (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Arquitetura do Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091004"
---
# <a name="windows-sockets-2-architecture"></a><span data-ttu-id="69ba5-103">Arquitetura do Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="69ba5-103">Windows Sockets 2 Architecture</span></span>

<span data-ttu-id="69ba5-104">A arquitetura do Windows Sockets 2 é compatível com a WOSA (arquitetura de sistema aberto do Windows), conforme ilustrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="69ba5-104">The Windows Sockets 2 architecture is compliant with the Windows Open System Architecture (WOSA), as illustrated below:</span></span>

![arquitetura do Windows Sockets 2](images/ovrvw2-1.png)

<span data-ttu-id="69ba5-106">O Winsock define uma SPI (interface de provedor de serviços) padrão entre a API (interface de programação de aplicativo), com suas funções exportadas de WS2 \_32.dll e as pilhas de protocolo.</span><span class="sxs-lookup"><span data-stu-id="69ba5-106">Winsock defines a standard service provider interface (SPI) between the application programming interface (API), with its functions exported from WS2\_32.dll and the protocol stacks.</span></span> <span data-ttu-id="69ba5-107">Consequentemente, o suporte a Winsock não está limitado a pilhas de protocolo TCP/IP como é o caso do Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="69ba5-107">Consequently, Winsock support is not limited to TCP/IP protocol stacks as is the case for Windows Sockets 1.1.</span></span>

<span data-ttu-id="69ba5-108">Com a arquitetura do Windows Sockets 2, não é necessário ou desejável, para que os fornecedores de pilha forneçam sua própria implementação de WS2 \_32.dll, já que uma única WS2 \_32.dll deve funcionar em todas as pilhas.</span><span class="sxs-lookup"><span data-stu-id="69ba5-108">With the Windows Sockets 2 architecture, it is not necessary or desirable, for stack vendors to supply their own implementation of WS2\_32.dll, since a single WS2\_32.dll must work across all stacks.</span></span> <span data-ttu-id="69ba5-109">O \_32.dll Ws2 e os shims de compatibilidade devem ser exibidos da mesma maneira que um componente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="69ba5-109">The WS2\_32.dll and compatibility shims should be viewed in the same way as an operating system component.</span></span>

 

 



