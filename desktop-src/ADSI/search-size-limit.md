---
title: Limite de tamanho de pesquisa
description: Para reduzir os requisitos de memória, um cliente pode se concentrar em um pequeno número de objetos retornados do servidor e ignorar o restante do conjunto de resultados.
ms.assetid: 675a4931-dfa4-4948-936b-dee27add530c
ms.tgt_platform: multiple
keywords:
- Limite de tamanho de pesquisa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd11148f9e887df1e15e221e8188f9e9e3b10d33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915886"
---
# <a name="search-size-limit"></a><span data-ttu-id="fdb69-104">Limite de tamanho de pesquisa</span><span class="sxs-lookup"><span data-stu-id="fdb69-104">Search Size Limit</span></span>

<span data-ttu-id="fdb69-105">Para reduzir os requisitos de memória, um cliente pode se concentrar em um pequeno número de objetos retornados do servidor e ignorar o restante do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="fdb69-105">To reduce memory requirements, a client can focus on a small number of objects returned from the server and ignore the rest of the result set.</span></span> <span data-ttu-id="fdb69-106">Para fazer isso, o cliente especifica um limite de tamanho de pesquisa e outros critérios de pesquisa apropriados.</span><span class="sxs-lookup"><span data-stu-id="fdb69-106">To accomplish this, the client specifies a search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="fdb69-107">Por exemplo, se um diretório armazena as pontuações de teste de um distrito escolar, você pode consultar os dez principais alunos com as pontuações de teste mais altas especificando um limite de tamanho de dez e uma ordem de classificação decrescente.</span><span class="sxs-lookup"><span data-stu-id="fdb69-107">For example, if a directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten and a descending sort order.</span></span>

<span data-ttu-id="fdb69-108">Para obter mais informações sobre como usar a opção de limite de tamanho de pesquisa com uma interface de pesquisa específica, consulte:</span><span class="sxs-lookup"><span data-stu-id="fdb69-108">For more information about using the search size limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="fdb69-109">Limite de tamanho com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="fdb69-109">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="fdb69-110">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="fdb69-110">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="fdb69-111">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="fdb69-111">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




