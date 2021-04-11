---
title: Usando funções de anti-aliasing
description: A tabela a seguir lista as funções de anti-aliasing do íris GL e suas funções OpenGL equivalentes.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Portabilidade do íris GL, anti-aliasing
- portando do íris GL, antialiasing
- portando para OpenGL do íris GL, antialiasing
- Portabilidade OpenGL do íris GL, antialiasing
- suavização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159616"
---
# <a name="using-antialiasing-functions"></a><span data-ttu-id="5e734-108">Usando funções de anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="5e734-108">Using Antialiasing Functions</span></span>

<span data-ttu-id="5e734-109">A tabela a seguir lista as funções de anti-aliasing do íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="5e734-109">The following table lists IRIS GL antialiasing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="5e734-110">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="5e734-110">IRIS GL function</span></span> | <span data-ttu-id="5e734-111">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="5e734-111">OpenGL function</span></span>                                      | <span data-ttu-id="5e734-112">Significado</span><span class="sxs-lookup"><span data-stu-id="5e734-112">Meaning</span></span>                           |
|------------------|------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="5e734-113">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="5e734-113">**pntsmooth**</span></span>    | <span data-ttu-id="5e734-114">[**glEnable**](glenable.md) ( \_ sem ajuste de ponto GL \_ )</span><span class="sxs-lookup"><span data-stu-id="5e734-114">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>   | <span data-ttu-id="5e734-115">Habilita a anti-aliasing de pontos.</span><span class="sxs-lookup"><span data-stu-id="5e734-115">Enables antialiasing of points.</span></span>   |
| <span data-ttu-id="5e734-116">**linesmooth**</span><span class="sxs-lookup"><span data-stu-id="5e734-116">**linesmooth**</span></span>   | <span data-ttu-id="5e734-117">**glEnable**( \_ linha simples de GL \_ )</span><span class="sxs-lookup"><span data-stu-id="5e734-117">**glEnable**( GL\_LINE\_SMOOTH )</span></span>                     | <span data-ttu-id="5e734-118">Habilita a anti-aliasing de linhas.</span><span class="sxs-lookup"><span data-stu-id="5e734-118">Enables antialiasing of lines.</span></span>    |
| <span data-ttu-id="5e734-119">**polismooth**</span><span class="sxs-lookup"><span data-stu-id="5e734-119">**polysmooth**</span></span>   | <span data-ttu-id="5e734-120">[**glEnable**](glenable.md) (uniforme do polígono do GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="5e734-120">[**glEnable**](glenable.md) ( GL\_POLYGON\_SMOOTH )</span></span> | <span data-ttu-id="5e734-121">Habilita a suavização de polígonos.</span><span class="sxs-lookup"><span data-stu-id="5e734-121">Enables antialiasing of polygons.</span></span> |



 

<span data-ttu-id="5e734-122">Use as chamadas [**glDisable**](gldisable.md) equivalentes para desativar a suavização.</span><span class="sxs-lookup"><span data-stu-id="5e734-122">Use the equivalent [**glDisable**](gldisable.md) calls to turn off antialiasing.</span></span>

<span data-ttu-id="5e734-123">No íris GL, você pode controlar a qualidade da suavização chamando:</span><span class="sxs-lookup"><span data-stu-id="5e734-123">In IRIS GL, you can control the quality of the antialiasing by calling:</span></span>


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



<span data-ttu-id="5e734-124">O OpenGL fornece [**glHint**](glhint.md)controluse semelhante:</span><span class="sxs-lookup"><span data-stu-id="5e734-124">OpenGL provides similar controluse [**glHint**](glhint.md):</span></span>


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



<span data-ttu-id="5e734-125">em que *hintmode* é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="5e734-125">where *hintMode* is one of the following:</span></span>

-   <span data-ttu-id="5e734-126">GL \_ mais interessante (use a suavização de qualidade mais alta.)</span><span class="sxs-lookup"><span data-stu-id="5e734-126">GL\_NICEST (Use the highest quality smoothing.)</span></span>
-   <span data-ttu-id="5e734-127">GL mais \_ rápido (use a suavização mais eficiente.)</span><span class="sxs-lookup"><span data-stu-id="5e734-127">GL\_FASTEST (Use the most efficient smoothing.)</span></span>
-   <span data-ttu-id="5e734-128">GL não se \_ \_ preocupa</span><span class="sxs-lookup"><span data-stu-id="5e734-128">GL\_DONT\_CARE</span></span>

<span data-ttu-id="5e734-129">O íris GL também permite a correção de fim chamando:</span><span class="sxs-lookup"><span data-stu-id="5e734-129">IRIS GL also permits end-correction by calling:</span></span>


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



<span data-ttu-id="5e734-130">O OpenGL não tem nenhum equivalente para essa função.</span><span class="sxs-lookup"><span data-stu-id="5e734-130">OpenGL has no equivalent for this function.</span></span>

 

 




