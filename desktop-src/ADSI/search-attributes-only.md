---
title: Pesquisar somente atributos
description: Às vezes, você executa uma pesquisa para determinar que tipo de dados está disponível para um objeto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Somente ADSI de atributos de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915887"
---
# <a name="search-attributes-only"></a><span data-ttu-id="e93fa-104">Pesquisar somente atributos</span><span class="sxs-lookup"><span data-stu-id="e93fa-104">Search Attributes Only</span></span>

<span data-ttu-id="e93fa-105">Às vezes, você executa uma pesquisa para determinar que tipo de dados está disponível para um objeto.</span><span class="sxs-lookup"><span data-stu-id="e93fa-105">Sometimes you perform a search to determine what type of data is available for an object.</span></span> <span data-ttu-id="e93fa-106">Nesse caso, você está interessado apenas nos atributos, e não nos valores do objeto.</span><span class="sxs-lookup"><span data-stu-id="e93fa-106">In this case, you are interested only in the attributes, and not the values, of the object.</span></span> <span data-ttu-id="e93fa-107">Para fazer isso, defina a opção "Pesquisar somente atributos".</span><span class="sxs-lookup"><span data-stu-id="e93fa-107">To accomplish this, you set the "search attributes only" option.</span></span> <span data-ttu-id="e93fa-108">A especificação dessa opção retorna os nomes de atributo sem seus valores.</span><span class="sxs-lookup"><span data-stu-id="e93fa-108">Specifying this option returns the attribute names without their values.</span></span> <span data-ttu-id="e93fa-109">No entanto, o conjunto de resultados inclui apenas os atributos que têm valores atribuídos.</span><span class="sxs-lookup"><span data-stu-id="e93fa-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="e93fa-110">Por exemplo, considere um objeto com os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="e93fa-110">For example, consider an object with the following attributes:</span></span>

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

<span data-ttu-id="e93fa-111">Quando a opção Pesquisar somente atributos é definida, o conjunto de resultados inclui:</span><span class="sxs-lookup"><span data-stu-id="e93fa-111">When the search attributes only option is set, the result set includes:</span></span>

``` syntax
First Name
Last Name
Phone Number
```

<span data-ttu-id="e93fa-112">Para obter mais informações sobre como usar a opção somente atributos de pesquisa com uma interface de pesquisa específica, consulte:</span><span class="sxs-lookup"><span data-stu-id="e93fa-112">For more information about using the search attributes only option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="e93fa-113">Retornando somente nomes de atributo com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="e93fa-113">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)
-   [<span data-ttu-id="e93fa-114">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="e93fa-114">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="e93fa-115">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="e93fa-115">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




