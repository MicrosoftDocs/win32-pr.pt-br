---
title: Usar identificadores de contexto para manter o estado no servidor
description: Usar identificadores de contexto para manter o estado no servidor
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159872"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a><span data-ttu-id="c568f-103">Usar identificadores de contexto para manter o estado no servidor</span><span class="sxs-lookup"><span data-stu-id="c568f-103">Use Context Handles for Keeping State on the Server</span></span>

<span data-ttu-id="c568f-104">**Prática recomendada:** Sempre que o estado for mantido no servidor entre as chamadas, use identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="c568f-104">**Best practice:** Whenever state is kept on the server between calls, use context handles.</span></span>

<span data-ttu-id="c568f-105">Os identificadores de contexto são geralmente intimidadores para novos programadores de RPC, e a sobrecarga dos identificadores de contexto de aprendizado pode não parecer ser o esforço inicialmente.</span><span class="sxs-lookup"><span data-stu-id="c568f-105">Context handles are often intimidating for new RPC programmers, and the overhead of learning context handles may not initially appear worth the effort.</span></span> <span data-ttu-id="c568f-106">Vale a pena que os identificadores de contexto tenham soluções internas para muitas armadilhas comuns encontradas na programação de rede que, de outra forma, teriam de ser implementadas do zero.</span><span class="sxs-lookup"><span data-stu-id="c568f-106">It is worth it because context handles have built-in solutions for many common pitfalls encountered in network programming that otherwise would have to be implemented from scratch.</span></span> <span data-ttu-id="c568f-107">Entender os indicadores de contexto paga dividendos mais tarde.</span><span class="sxs-lookup"><span data-stu-id="c568f-107">Understanding context handles pays dividends later.</span></span>

 

 




