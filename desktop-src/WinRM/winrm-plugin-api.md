---
title: API de plug-in do WinRM
description: A API (interface de programação de aplicativo) de plug-in do WinRM fornece funcionalidade que permite que um usuário escreva plug-ins implementando determinadas APIs para operações e URIs de recursos com suporte.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916429"
---
# <a name="winrm-plug-in-api"></a><span data-ttu-id="1ef09-103">API de plug-in do WinRM</span><span class="sxs-lookup"><span data-stu-id="1ef09-103">WinRM Plug-in API</span></span>

<span data-ttu-id="1ef09-104">Os plug-ins Gerenciamento Remoto do Windows são DLLs (bibliotecas de vínculo dinâmico) nativas que se conectam e estendem a funcionalidade do WinRM.</span><span class="sxs-lookup"><span data-stu-id="1ef09-104">Windows Remote Management plug-ins are native dynamic-link libraries (DLLs) that plug into and extend the functionality of WinRM.</span></span> <span data-ttu-id="1ef09-105">A API (interface de programação de aplicativo) de plug-in do WinRM fornece funcionalidade que permite que um usuário escreva plug-ins implementando determinadas APIs para operações e [*URIs de recursos*](windows-remote-management-glossary.md) com suporte.</span><span class="sxs-lookup"><span data-stu-id="1ef09-105">The WinRM Plug-in application programming interface (API) provides functionality that enables a user to write plug-ins by implementing certain APIs for supported [*resource URIs*](windows-remote-management-glossary.md) and operations.</span></span> <span data-ttu-id="1ef09-106">Depois que os plug-ins são configurados para o serviço WinRM ou Serviços de Informações da Internet (IIS), eles são carregados no host do WinRM ou host do IIS, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1ef09-106">After the plug-ins are configured for either the WinRM service or Internet Information Services (IIS), they are loaded into the WinRM host or IIS host, respectively.</span></span> <span data-ttu-id="1ef09-107">As solicitações remotas são roteadas para esses pontos de entrada de plug-in para executar operações.</span><span class="sxs-lookup"><span data-stu-id="1ef09-107">Remote requests are routed to these plug-in entry points to carry out operations.</span></span>

<span data-ttu-id="1ef09-108">A seção de referência da API de plug-in do WinRM contém informações detalhadas sobre os seguintes elementos de API:</span><span class="sxs-lookup"><span data-stu-id="1ef09-108">The WinRM Plug-in API reference section contains detailed information about the following API elements:</span></span>

-   [<span data-ttu-id="1ef09-109">Pontos de entrada de plug-in de autorização</span><span class="sxs-lookup"><span data-stu-id="1ef09-109">Authorization Plug-in Entry Points</span></span>](authorization-plug-in-entry-points.md)
-   [<span data-ttu-id="1ef09-110">Métodos de plug-in de autorização</span><span class="sxs-lookup"><span data-stu-id="1ef09-110">Authorization Plug-in Methods</span></span>](authorization-plug-in-methods.md)
-   [<span data-ttu-id="1ef09-111">Pontos de entrada de plug-in de operações</span><span class="sxs-lookup"><span data-stu-id="1ef09-111">Operations Plug-in Entry Points</span></span>](operations-plug-in-entry-points.md)
-   [<span data-ttu-id="1ef09-112">Métodos de plug-in de operações</span><span class="sxs-lookup"><span data-stu-id="1ef09-112">Operations Plug-in Methods</span></span>](operations-plug-in-methods.md)
-   [<span data-ttu-id="1ef09-113">Estruturas</span><span class="sxs-lookup"><span data-stu-id="1ef09-113">Structures</span></span>](winrm-plug-in-api-structures.md)

 

 




