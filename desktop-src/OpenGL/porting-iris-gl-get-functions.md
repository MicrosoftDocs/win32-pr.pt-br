---
title: Funções Get GL do íris de portabilidade
description: ÍRIS GL \ 0034; Get \ 0034; as funções usam o seguinte formulário
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Portabilidade do íris GL, obter funções
- portando do íris GL, obter funções
- portando para OpenGL do íris GL, obter funções
- Portabilidade do OpenGL do íris GL, obter funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105762925"
---
# <a name="porting-iris-gl-get-functions"></a><span data-ttu-id="c02ee-107">Funções Get GL do íris de portabilidade</span><span class="sxs-lookup"><span data-stu-id="c02ee-107">Porting IRIS GL Get Functions</span></span>

<span data-ttu-id="c02ee-108">As funções de "Get" da íris GL assumem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="c02ee-108">IRIS GL "get" functions take the following form:</span></span>

``` syntax
int getthing();
```

<span data-ttu-id="c02ee-109">e</span><span class="sxs-lookup"><span data-stu-id="c02ee-109">and</span></span>

``` syntax
int getthings( int *a, int *b);
```

<span data-ttu-id="c02ee-110">O código da íris GL provavelmente incluirá chamadas de função Get parecidas com:</span><span class="sxs-lookup"><span data-stu-id="c02ee-110">Your IRIS GL code probably includes get function calls that look something like:</span></span>

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

<span data-ttu-id="c02ee-111">No OpenGL, você usa um dos quatro tipos de funções [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) a seguir em vez de funções Get GL equivalentes de íris.</span><span class="sxs-lookup"><span data-stu-id="c02ee-111">In OpenGL you use one of the following four types of [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) functions in place of equivalent IRIS GL get functions:</span></span>

-   <span data-ttu-id="c02ee-112">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="c02ee-112">**glGetBooleanv**</span></span>
-   <span data-ttu-id="c02ee-113">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="c02ee-113">**glGetIntegerv**</span></span>
-   <span data-ttu-id="c02ee-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="c02ee-114">**glGetFloatv**</span></span>
-   <span data-ttu-id="c02ee-115">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="c02ee-115">**glGetDoublev**</span></span>

<span data-ttu-id="c02ee-116">As funções têm a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="c02ee-116">The functions have the following syntax:</span></span>

``` syntax
glGet<Datatype>v( value, *data );
```

<span data-ttu-id="c02ee-117">em que *Value* é do tipo **GLenum** e os dados são do tipo **GLdatatype**.</span><span class="sxs-lookup"><span data-stu-id="c02ee-117">where *value* is of type **GLenum** and data is of type **GLdatatype**.</span></span> <span data-ttu-id="c02ee-118">Quando você chama **glGet** e retorna um tipo diferente do tipo esperado, o tipo é convertido adequadamente.</span><span class="sxs-lookup"><span data-stu-id="c02ee-118">When you call **glGet** and it returns a type different from the type expected, the type is converted appropriately.</span></span> <span data-ttu-id="c02ee-119">Para obter uma lista completa de parâmetros de **glGet** , consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="c02ee-119">For a complete list of **glGet** parameters, see [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span></span>

 

 




