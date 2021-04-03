---
title: Recuperação de intervalo de atributos
description: Um atributo com valores múltiplos pode ter quase qualquer número de valores. Em muitos casos, pode ser vantajoso, ou até mesmo necessário, limitar o intervalo de valores que são recuperados por uma consulta.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI de recuperação de intervalo de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915915"
---
# <a name="attribute-range-retrieval"></a><span data-ttu-id="a9e47-105">Recuperação de intervalo de atributos</span><span class="sxs-lookup"><span data-stu-id="a9e47-105">Attribute Range Retrieval</span></span>

<span data-ttu-id="a9e47-106">Um atributo com valores múltiplos pode ter quase qualquer número de valores.</span><span class="sxs-lookup"><span data-stu-id="a9e47-106">A multi-valued attribute can have almost any number of values.</span></span> <span data-ttu-id="a9e47-107">Em muitos casos, pode ser vantajoso, ou até mesmo necessário, limitar o intervalo de valores que são recuperados por uma consulta.</span><span class="sxs-lookup"><span data-stu-id="a9e47-107">In many cases, it may be advantageous, or even necessary, to limit the range of values that are retrieved by a query.</span></span>

<span data-ttu-id="a9e47-108">A recuperação de intervalo envolve a solicitação de um número limitado de valores de atributo em uma única consulta.</span><span class="sxs-lookup"><span data-stu-id="a9e47-108">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="a9e47-109">O número de valores solicitados deve ser menor ou igual ao número máximo de valores com suporte pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="a9e47-109">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="a9e47-110">Para reduzir o número de vezes que a consulta deve entrar em contato com o servidor, o número de valores solicitados deve ser o mais próximo possível do máximo possível.</span><span class="sxs-lookup"><span data-stu-id="a9e47-110">To reduce the number of times the query must contact the server, the number of values requested should be as close to this maximum as possible.</span></span> <span data-ttu-id="a9e47-111">Para permitir que um aplicativo funcione corretamente com todos os servidores Windows, um número máximo de 1000 deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="a9e47-111">To enable an application to work correctly with all Windows servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="a9e47-112">Os especificadores de intervalo para uma consulta de propriedade exigem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a9e47-112">The range specifiers for a property query require the following form:</span></span>


```C++
range=<low range>-<high range>
```



<span data-ttu-id="a9e47-113">em que " &lt; intervalo baixo &gt; " é o índice de base zero do primeiro valor da propriedade a ser recuperado e " &lt; intervalo alto &gt; " é o índice de base zero do último valor da propriedade a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="a9e47-113">where "&lt;low range&gt;" is the zero-based index of the first property value to retrieve and "&lt;high range&gt;" is the zero-based index of the last property value to retrieve.</span></span> <span data-ttu-id="a9e47-114">Zero é usado para " &lt; intervalo baixo &gt; " para especificar a primeira entrada.</span><span class="sxs-lookup"><span data-stu-id="a9e47-114">Zero is used for "&lt;low range&gt;" to specify the first entry.</span></span> <span data-ttu-id="a9e47-115">O caractere curinga ( \* ) pode ser usado para " &lt; intervalo alto &gt; " para especificar todas as entradas restantes.</span><span class="sxs-lookup"><span data-stu-id="a9e47-115">The wildcard character (\*) can be used for "&lt;high range&gt;" to specify all remaining entries.</span></span>

<span data-ttu-id="a9e47-116">A tabela a seguir lista exemplos de especificadores de intervalo.</span><span class="sxs-lookup"><span data-stu-id="a9e47-116">The following table lists examples of range specifiers.</span></span>



| <span data-ttu-id="a9e47-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a9e47-117">Example</span></span>      | <span data-ttu-id="a9e47-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9e47-118">Description</span></span>                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e47-119">intervalo = 0-\*</span><span class="sxs-lookup"><span data-stu-id="a9e47-119">range=0-\*</span></span>   | <span data-ttu-id="a9e47-120">Recupere todos os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a9e47-120">Retrieve all property values.</span></span> <span data-ttu-id="a9e47-121">Isso está sujeito a limites impostos pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="a9e47-121">This is subject to limits imposed by the server.</span></span>                |
| <span data-ttu-id="a9e47-122">intervalo = 0-500</span><span class="sxs-lookup"><span data-stu-id="a9e47-122">range=0-500</span></span>  | <span data-ttu-id="a9e47-123">Recupere de 1 a 501st valores inclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a9e47-123">Retrieve from 1st to 501st values inclusively.</span></span>                                                |
| <span data-ttu-id="a9e47-124">intervalo = 2-3</span><span class="sxs-lookup"><span data-stu-id="a9e47-124">range=2-3</span></span>    | <span data-ttu-id="a9e47-125">Recupere os 3 e 4º valores.</span><span class="sxs-lookup"><span data-stu-id="a9e47-125">Retrieve 3rd and 4th values.</span></span>                                                                  |
| <span data-ttu-id="a9e47-126">intervalo = 501-\*</span><span class="sxs-lookup"><span data-stu-id="a9e47-126">range=501-\*</span></span> | <span data-ttu-id="a9e47-127">Recupere o 502nd e todos os valores restantes.</span><span class="sxs-lookup"><span data-stu-id="a9e47-127">Retrieve the 502nd and all remaining values.</span></span> <span data-ttu-id="a9e47-128">Isso está sujeito a limites impostos pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="a9e47-128">This is subject to limits imposed by the server.</span></span> |



 

<span data-ttu-id="a9e47-129">Há várias maneiras diferentes de recuperar um intervalo de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a9e47-129">There are several different ways to retrieve a range of property values.</span></span> <span data-ttu-id="a9e47-130">O método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pode ser usado em uma linguagem de automação ou em um C++.</span><span class="sxs-lookup"><span data-stu-id="a9e47-130">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method can be used in either an automation language or C++.</span></span> <span data-ttu-id="a9e47-131">O método **IADs. GetInfoEx** é o método preferencial para executar a recuperação de intervalo.</span><span class="sxs-lookup"><span data-stu-id="a9e47-131">The **IADs.GetInfoEx** method is the preferred method of performing range retrieval.</span></span> <span data-ttu-id="a9e47-132">Para obter mais informações sobre como usar **IADs. GetInfoEx** para recuperação de intervalo, consulte [usando IADs:: GetInfoEx para recuperação de intervalo](using-iads--getinfoex-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="a9e47-132">For more information about using **IADs.GetInfoEx** for range retrieval, see [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).</span></span>

<span data-ttu-id="a9e47-133">Se um idioma de automação for usado, o ADO (objetos de diretório do ActiveX) poderá ser usado para recuperar um intervalo de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a9e47-133">If an automation language is used, the ActiveX Directory Objects (ADO) can be used to retrieve a range of property values.</span></span> <span data-ttu-id="a9e47-134">Para obter mais informações sobre como usar o ADO para recuperação de intervalo, consulte [usando ADO para recuperação de intervalo](using-ado-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="a9e47-134">For more information about using ADO for range retrieval, see [Using ADO for Range Retrieval](using-ado-for-range-retrieval.md).</span></span>

<span data-ttu-id="a9e47-135">Se o C++ for usado, as interfaces [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) e [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) poderão ser usadas para recuperar um intervalo de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a9e47-135">If C++ is used, the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) and [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="a9e47-136">Para obter mais informações sobre como usar **IDirectorySearch** e **IDirectoryObject** para recuperação de intervalo, consulte [usando IDirectorySearch e IDirectoryObject para recuperação de intervalo](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="a9e47-136">For more information about using **IDirectorySearch** and **IDirectoryObject** for range retrieval, see [Using IDirectorySearch and IDirectoryObject for Range Retrieval](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span></span>

 

 




