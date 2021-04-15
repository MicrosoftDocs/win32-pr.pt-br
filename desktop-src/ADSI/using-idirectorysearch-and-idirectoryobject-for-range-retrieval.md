---
title: Usando IDirectorySearch e IDirectoryObject para recuperação de intervalo
description: As interfaces IDirectoryObject ou IDirectorySearch podem ser usadas para recuperar um intervalo de valores de propriedade. Para fazer isso, especifique o atributo e o intervalo para um dos atributos solicitados na consulta.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI, usando para a variação para recuperar membros de um grupo
- IDirectoryObject ADSI, usando para a variação para recuperar membros de um grupo
- ADSI de recuperação de intervalo, usando IDirectorySearch e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754013"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a><span data-ttu-id="73d59-107">Usando IDirectorySearch e IDirectoryObject para recuperação de intervalo</span><span class="sxs-lookup"><span data-stu-id="73d59-107">Using IDirectorySearch and IDirectoryObject for Range Retrieval</span></span>

<span data-ttu-id="73d59-108">As interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ou [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) podem ser usadas para recuperar um intervalo de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="73d59-108">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) or [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="73d59-109">Para fazer isso, especifique o atributo e o intervalo para um dos atributos solicitados na consulta.</span><span class="sxs-lookup"><span data-stu-id="73d59-109">To do this, specify the attribute and range for one of the attributes requested in the query.</span></span>

## <a name="range-retrieval-with-idirectoryobject"></a><span data-ttu-id="73d59-110">Recuperação de intervalo com IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="73d59-110">Range Retrieval with IDirectoryObject</span></span>

<span data-ttu-id="73d59-111">A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pode ser usada para recuperação de intervalo, especificando o atributo e o intervalo para um dos atributos na matriz *pAttributesName* ao chamar o método [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="73d59-111">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface can be used for range retrieval by specifying the attribute and range for one of the attributes in the *pAttributesName* array when calling the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



<span data-ttu-id="73d59-112">Para obter mais informações e um exemplo de código que mostra como usar a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para recuperação de intervalo, consulte o [código de exemplo para variar com IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="73d59-112">For more information and a code example that shows how to use the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for range retrieval, see [Example Code for Ranging with IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span></span>

## <a name="range-retrieval-with-idirectorysearch"></a><span data-ttu-id="73d59-113">Recuperação de intervalo com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73d59-113">Range Retrieval with IDirectorySearch</span></span>

<span data-ttu-id="73d59-114">A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pode ser usada para recuperação de intervalo, especificando o atributo e o intervalo para um dos atributos recuperados na matriz *pAttributesName* ao chamar o método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="73d59-114">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface can be used for range retrieval by specifying the attribute and range for one of the retrieved attributes in the *pAttributesName* array when calling the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method.</span></span>


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



<span data-ttu-id="73d59-115">Ao usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para recuperação de intervalo, há um problema que deve ser resolvido especificamente.</span><span class="sxs-lookup"><span data-stu-id="73d59-115">When using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="73d59-116">Quando o intervalo solicitado excede o número de valores restantes, [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) retornará a **\_ coluna ADS \_ E \_ não \_ definida**.</span><span class="sxs-lookup"><span data-stu-id="73d59-116">When the range requested exceeds the number of remaining values, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="73d59-117">Para recuperar os valores restantes, é necessário usar o curinga de intervalo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="73d59-117">To retrieve the remaining values, it is necessary to use the range wildcard '\*'.</span></span> <span data-ttu-id="73d59-118">Por exemplo, se um grupo contiver 150 Membros, os valores de membro 0-100 poderão ser recuperados normalmente usando a recuperação em intervalos.</span><span class="sxs-lookup"><span data-stu-id="73d59-118">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="73d59-119">Se o intervalo 101-200 for solicitado, **IDirectorySearch:: GetColumn** retornará **E a \_ \_ coluna ADS \_ não será \_ definida**.</span><span class="sxs-lookup"><span data-stu-id="73d59-119">If range 101-200 is then requested, **IDirectorySearch::GetColumn** will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="73d59-120">Esse problema pode ser evitado usando o método [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) .</span><span class="sxs-lookup"><span data-stu-id="73d59-120">This problem can be avoided by using the [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) method.</span></span> <span data-ttu-id="73d59-121">Normalmente, **GetNextColumnName** retornará a cadeia de caracteres de consulta original.</span><span class="sxs-lookup"><span data-stu-id="73d59-121">Normally, **GetNextColumnName** will return the original query string.</span></span> <span data-ttu-id="73d59-122">No entanto, quando o intervalo solicitado excede o número de valores restantes, **GetNextColumnName** retornará uma versão modificada da cadeia de caracteres de consulta, substituindo o valor de intervalo alto pelo curinga de intervalo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="73d59-122">However, when the range requested exceeds the number of remaining values, **GetNextColumnName** will return a modified version of the query string by replacing the high range value with the range wildcard '\*'.</span></span> <span data-ttu-id="73d59-123">No exemplo acima, a primeira consulta seria executada com uma cadeia de caracteres de atributo "membro; intervalo = 0-100" e **GetNextColumnName** retornará "membro; intervalo = 0-100".</span><span class="sxs-lookup"><span data-stu-id="73d59-123">In the example above, the first query would be performed with an attribute string of "member;range=0-100" and **GetNextColumnName** will return "member;range=0-100".</span></span> <span data-ttu-id="73d59-124">Na segunda consulta, a cadeia de caracteres do atributo seria "membro; intervalo = 101-200", mas **GetNextColumnName** retornará "membro; intervalo = 101- \* ".</span><span class="sxs-lookup"><span data-stu-id="73d59-124">In the second query, the attribute string would be "member;range=101-200", but **GetNextColumnName** will return "member;range=101-\*".</span></span> <span data-ttu-id="73d59-125">Esse caso pode ser determinado comparando a cadeia de caracteres do atributo original com o resultado de **GetNextColumnName**.</span><span class="sxs-lookup"><span data-stu-id="73d59-125">This case can be determined by comparing the original attribute string to the result of **GetNextColumnName**.</span></span> <span data-ttu-id="73d59-126">Se as cadeias de caracteres forem diferentes, o último bloco de valores deverá ser solicitado novamente com o curinga de intervalo.</span><span class="sxs-lookup"><span data-stu-id="73d59-126">If the strings are different, the last block of values should be requested again with the range wildcard.</span></span>

<span data-ttu-id="73d59-127">Para obter mais informações e um exemplo de código que mostra como usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para recuperação de intervalo, consulte o [código de exemplo para variar com IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="73d59-127">For more information and a code example that shows how to use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, see [Example Code for Ranging with IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span></span>

 

 




