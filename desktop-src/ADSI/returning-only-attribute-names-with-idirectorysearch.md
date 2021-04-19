---
title: Retornando somente nomes de atributo com IDirectorySearch
description: Você pode executar uma pesquisa para determinar que tipo de dados está disponível para um determinado objeto.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Retornando somente nomes de atributo com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, retornando apenas nomes de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105749383"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a><span data-ttu-id="5195b-105">Retornando somente nomes de atributo com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="5195b-105">Returning Only Attribute Names with IDirectorySearch</span></span>

<span data-ttu-id="5195b-106">Você pode executar uma pesquisa para determinar que tipo de dados está disponível para um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="5195b-106">You can perform a search to determine what type of data is available for a particular object.</span></span> <span data-ttu-id="5195b-107">Nesse caso, você está interessado apenas nos nomes dos atributos, não nos valores de atributo do objeto.</span><span class="sxs-lookup"><span data-stu-id="5195b-107">In this case, you are only interested in the attributes names, not the attribute values of the object.</span></span> <span data-ttu-id="5195b-108">A opção **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ somente** faz com que o servidor retorne apenas os nomes de atributo e não os valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="5195b-108">The **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option causes the server to only return the attribute names and not the attribute values.</span></span> <span data-ttu-id="5195b-109">No entanto, o conjunto de resultados inclui apenas os atributos que têm valores atribuídos.</span><span class="sxs-lookup"><span data-stu-id="5195b-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="5195b-110">Por exemplo, considere um objeto com os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="5195b-110">For example, consider an object with the following attributes:</span></span>

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

<span data-ttu-id="5195b-111">Quando a opção **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ somente** é definida, o conjunto de resultados inclui:</span><span class="sxs-lookup"><span data-stu-id="5195b-111">When the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option is set, the result set includes:</span></span>

``` syntax
name
sn
department
phone
```

<span data-ttu-id="5195b-112">O padrão é que os valores de atributo e os nomes sejam retornados.</span><span class="sxs-lookup"><span data-stu-id="5195b-112">The default is for both attribute values and names to be returned.</span></span>

<span data-ttu-id="5195b-113">Para recuperar apenas os nomes de atributo, defina uma opção de pesquisa **\_ \_ \_ somente ADS SEARCHPREF ATTRIBTYPES** com um valor **\_ booliano de ADSTYPE** **true** na matriz de [**informações do ADS \_ \_ SEARCHPREF**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="5195b-113">To retrieve only attribute names, set an **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="5195b-114">O exemplo de código a seguir mostra como recuperar somente nomes de atributo.</span><span class="sxs-lookup"><span data-stu-id="5195b-114">The following code example shows how to retrieve attribute names only.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



<span data-ttu-id="5195b-115">Para obter mais informações e um exemplo de código que mostra como usar a opção de pesquisa **\_ \_ \_ somente ATTRIBTYPES do ADS SEARCHPREF** , consulte o [código de exemplo para pesquisar atributos](example-code-for-searching-for-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="5195b-115">For more information and a code example that shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option, see [Example Code for Searching for Attributes](example-code-for-searching-for-attributes.md).</span></span>

 

 




