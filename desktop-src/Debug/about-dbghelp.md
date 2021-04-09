---
description: Os tópicos a seguir descrevem arquivos de símbolo e a funcionalidade fornecida pelas funções DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Sobre o DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089020"
---
# <a name="about-dbghelp"></a><span data-ttu-id="5db69-103">Sobre o DbgHelp</span><span class="sxs-lookup"><span data-stu-id="5db69-103">About DbgHelp</span></span>

<span data-ttu-id="5db69-104">Os tópicos a seguir descrevem arquivos de símbolo e a funcionalidade fornecida pelas [funções dbghelp](dbghelp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5db69-104">The following topics describe symbol files and the functionality provided by the [DbgHelp functions](dbghelp-functions.md).</span></span>

-   [<span data-ttu-id="5db69-105">Versões do DbgHelp</span><span class="sxs-lookup"><span data-stu-id="5db69-105">DbgHelp Versions</span></span>](dbghelp-versions.md)
-   [<span data-ttu-id="5db69-106">Arquivos de Símbolo</span><span class="sxs-lookup"><span data-stu-id="5db69-106">Symbol Files</span></span>](symbol-files.md)
-   [<span data-ttu-id="5db69-107">Manipulação de símbolos</span><span class="sxs-lookup"><span data-stu-id="5db69-107">Symbol Handling</span></span>](symbol-handling.md)
-   [<span data-ttu-id="5db69-108">Servidores de símbolos e armazenamentos de símbolos</span><span class="sxs-lookup"><span data-stu-id="5db69-108">Symbol Servers and Symbol Stores</span></span>](symbol-servers-and-symbol-stores.md)
-   [<span data-ttu-id="5db69-109">Arquivos de minidespejo</span><span class="sxs-lookup"><span data-stu-id="5db69-109">Minidump Files</span></span>](minidump-files.md)
-   [<span data-ttu-id="5db69-110">Servidor de origem</span><span class="sxs-lookup"><span data-stu-id="5db69-110">Source Server</span></span>](source-server-and-source-indexing.md)
-   [<span data-ttu-id="5db69-111">Suporte atualizado à plataforma</span><span class="sxs-lookup"><span data-stu-id="5db69-111">Updated Platform Support</span></span>](updated-platform-support.md)

<span data-ttu-id="5db69-112">Observe que todas as [funções dbghelp](dbghelp-functions.md) são thread único.</span><span class="sxs-lookup"><span data-stu-id="5db69-112">Note that all [DbgHelp functions](dbghelp-functions.md) are single threaded.</span></span> <span data-ttu-id="5db69-113">Portanto, as chamadas de mais de um thread para essa função provavelmente resultarão em um comportamento inesperado ou corrupção de memória.</span><span class="sxs-lookup"><span data-stu-id="5db69-113">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="5db69-114">Para evitar isso, você deve sincronizar todas as chamadas simultâneas de mais de um thread para essa função.</span><span class="sxs-lookup"><span data-stu-id="5db69-114">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

 

 



