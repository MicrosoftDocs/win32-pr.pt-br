---
title: Como funciona a indexação de tupla
description: Os índices de tupla são usados para otimizar as pesquisas que têm 0 ou mais cadeias de caracteres de pesquisa de média e 0 ou 1 cadeias de caracteres de pesquisa final. Eles também podem ser usados para otimizar as pesquisas de uma cadeia de caracteres de pesquisa inicial se nenhum índice comum estiver disponível nesse atributo.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indexação de tupla
- Pesquisando Active Directory Active Directory, otimização
- Active Directory, Active Directory de otimização da pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640396"
---
# <a name="how-tuple-indexing-works"></a><span data-ttu-id="5a0fb-107">Como funciona a indexação de tupla</span><span class="sxs-lookup"><span data-stu-id="5a0fb-107">How Tuple Indexing Works</span></span>

<span data-ttu-id="5a0fb-108">Os índices de tupla são usados para otimizar as pesquisas que têm 0 ou mais [cadeias de caracteres de pesquisa de média](search-string-types.md) e 0 ou 1 cadeias de caracteres de pesquisa final.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-108">Tuple indices are used to optimize searches that have 0 or more [medial-search strings](search-string-types.md) and 0 or 1 final-search strings.</span></span> <span data-ttu-id="5a0fb-109">Eles também podem ser usados para otimizar as pesquisas de uma cadeia de caracteres de pesquisa inicial se nenhum índice comum estiver disponível nesse atributo.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-109">They can also be used to optimize searches for an initial search string if no ordinary index is available over that attribute.</span></span>

<span data-ttu-id="5a0fb-110">Você pode ativar a indexação de tupla para um atributo definindo o bit 5, que corresponde ao valor 32, no atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .</span><span class="sxs-lookup"><span data-stu-id="5a0fb-110">You can turn on tuple indexing for an attribute by setting bit 5, which corresponds to the value 32, in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute.</span></span> <span data-ttu-id="5a0fb-111">Esse atributo é definido no objeto de esquema que representa o atributo que precisa do índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-111">This attribute is set in the schema object that represents the attribute that needs the tuple index.</span></span> <span data-ttu-id="5a0fb-112">O impacto no desempenho de ativar a indexação de tupla é que qualquer valor de cadeia de caracteres definido para esse atributo será expandido em um grande número de fragmentos no índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-112">The performance impact of turning on tuple indexing is that any string value that is set for that attribute will be expanded into a large number of fragments in the tuple index.</span></span> <span data-ttu-id="5a0fb-113">Quando um atributo é expandido, ele consome uma quantidade maior de espaço em disco no arquivo da árvore de informações do diretório e também é atualizado mais lentamente.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-113">When an attribute expands, it consumes a larger amount of disk space in the Directory Information Tree file, and also gets updated more slowly.</span></span>

<span data-ttu-id="5a0fb-114">Os índices de tupla são projetados para acelerar as pesquisas do formulário `*string*` .</span><span class="sxs-lookup"><span data-stu-id="5a0fb-114">Tuple indices are designed to accelerate searches of the form `*string*`.</span></span> <span data-ttu-id="5a0fb-115">A aceleração pode ser considerável, pois essa forma de pesquisa não pode ser otimizada de nenhuma outra maneira e, em seu formato não otimizado, força o servidor de Active Directory a percorrer cada objeto no escopo da pesquisa para executar a consulta.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-115">The acceleration can be considerable because this form of search cannot be optimized in any other way, and in its un-optimized form, it forces the Active Directory server to walk every object in the scope of the search to perform the query.</span></span> <span data-ttu-id="5a0fb-116">Portanto, uma pesquisa de base simplesmente pesquisaria um objeto, que usaria menos recursos, uma pesquisa de filhos imediata pesquisaria apenas os filhos de um objeto (o que poderia usar menos recursos ou mais recursos, dependendo do tamanho do contêiner), e uma pesquisa de subárvore percorrerá toda a subárvore sob o objeto base, o que geralmente exigiria muitos recursos e seria muito lento devido ao tamanho</span><span class="sxs-lookup"><span data-stu-id="5a0fb-116">Thus, a base search would just search one object, which would use fewer resources, an immediate children search would search just the children of an object (which could use fewer resources or more resources depending on the container size), and a subtree search will walk the entire subtree under the base object, which would usually require a lot of resources and be very slow because of the subtree size.</span></span>

<span data-ttu-id="5a0fb-117">Os índices de tupla funcionam dividindo uma cadeia de caracteres em *tuplas*.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-117">Tuple indices work by breaking a string into *tuples*.</span></span> <span data-ttu-id="5a0fb-118">Por exemplo, a cadeia de caracteres "Active Directory" seria dividida nas seguintes tuplas:</span><span class="sxs-lookup"><span data-stu-id="5a0fb-118">For example, the string "Active Directory" would be broken into the following tuples:</span></span>

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> <span data-ttu-id="5a0fb-119">O diretório será interrompido em 32767 caracteres ao expandir uma cadeia de caracteres para indexação de tupla.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-119">The directory will stop at 32767 characters when expanding a string for tuple indexing.</span></span>

 

<span data-ttu-id="5a0fb-120">Um índice de tupla conterá uma entrada para cada uma dessas tuplas.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-120">A tuple index would contain an entry for each one of these tuples.</span></span> <span data-ttu-id="5a0fb-121">Portanto, se um usuário procurar `*cto*` , o servidor de Active Directory pesquisará todas as correspondências para "CTO" no índice e, nesse caso, localizará um ponteiro de volta para o registro que tinha um atributo (tupla indexada) com um valor de "Directory".</span><span class="sxs-lookup"><span data-stu-id="5a0fb-121">So, if a user searches for `*cto*`, then the Active Directory server will look up all the matches for "cto" in the index and, in this case, find a pointer back to the record that had a (tuple indexed) attribute with a value of "Directory".</span></span>

<span data-ttu-id="5a0fb-122">Se a cadeia de caracteres de pesquisa medial ( `*cto*` no exemplo anterior) for específica o suficiente, a pesquisa será bastante eficiente, pois reduz consideravelmente o número de objetos que o servidor de Active Directory deve inspecionar para executar a consulta.</span><span class="sxs-lookup"><span data-stu-id="5a0fb-122">If the medial search string (`*cto*` in the previous example) is specific enough, then the search will be quite efficient because it greatly reduces the number of objects that the Active Directory server must inspect to perform the query.</span></span>

 

 