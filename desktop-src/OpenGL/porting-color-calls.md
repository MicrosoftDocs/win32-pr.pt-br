---
title: Portando chamadas de cores
description: A tabela a seguir lista as funções de cor do íris GL e suas funções OpenGL equivalentes.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Portabilidade do íris GL, cor
- portando do íris GL, cor
- portando para OpenGL do íris GL, cor
- Portabilidade do OpenGL do íris GL, cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635223"
---
# <a name="porting-color-calls"></a><span data-ttu-id="d5227-107">Portando chamadas de cores</span><span class="sxs-lookup"><span data-stu-id="d5227-107">Porting Color Calls</span></span>

<span data-ttu-id="d5227-108">A tabela a seguir lista as funções de cor do íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="d5227-108">The following table lists IRIS GL color functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="d5227-109">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="d5227-109">IRIS GL function</span></span>                  | <span data-ttu-id="d5227-110">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="d5227-110">OpenGL function</span></span>                                                                                                                               | <span data-ttu-id="d5227-111">Significado</span><span class="sxs-lookup"><span data-stu-id="d5227-111">Meaning</span></span>                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5227-112">**c**</span><span class="sxs-lookup"><span data-stu-id="d5227-112">**c**</span></span>                             | [<span data-ttu-id="d5227-113">glColor</span><span class="sxs-lookup"><span data-stu-id="d5227-113">glColor</span></span>](glcolor-functions.md)                                                                                                              | <span data-ttu-id="d5227-114">Define a cor RGB.</span><span class="sxs-lookup"><span data-stu-id="d5227-114">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="d5227-115">**color**</span><span class="sxs-lookup"><span data-stu-id="d5227-115">**color**</span></span>                         | [<span data-ttu-id="d5227-116">glIndex</span><span class="sxs-lookup"><span data-stu-id="d5227-116">glIndex</span></span>](glindex-functions.md)                                                                                                              | <span data-ttu-id="d5227-117">Define o índice de cores.</span><span class="sxs-lookup"><span data-stu-id="d5227-117">Sets the color index.</span></span>                                |
| <span data-ttu-id="d5227-118">**GetColor**</span><span class="sxs-lookup"><span data-stu-id="d5227-118">**getcolor**</span></span>                      | <span data-ttu-id="d5227-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ índice atual do GL \_ )</span><span class="sxs-lookup"><span data-stu-id="d5227-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_CURRENT\_INDEX )</span></span>                                               | <span data-ttu-id="d5227-120">Retorna o índice de cores atual.</span><span class="sxs-lookup"><span data-stu-id="d5227-120">Returns the current color index.</span></span>                     |
| <span data-ttu-id="d5227-121">**getmcolor**</span><span class="sxs-lookup"><span data-stu-id="d5227-121">**getmcolor**</span></span>                     |                                                                                                                                               | <span data-ttu-id="d5227-122">Obtém uma cópia dos valores RGB para uma entrada de mapa de cores.</span><span class="sxs-lookup"><span data-stu-id="d5227-122">Gets a copy of the RGB values for a color map entry.</span></span> |
| <span data-ttu-id="d5227-123">**gRGBcolor**</span><span class="sxs-lookup"><span data-stu-id="d5227-123">**gRGBcolor**</span></span>                     | <span data-ttu-id="d5227-124">**glGet**( \_ cor atual do GL \_ )</span><span class="sxs-lookup"><span data-stu-id="d5227-124">**glGet**( GL\_CURRENT\_COLOR )</span></span>                                                                                                               | <span data-ttu-id="d5227-125">Obtém os valores de cor RGB atuais.</span><span class="sxs-lookup"><span data-stu-id="d5227-125">Gets the current RGB color values.</span></span>                   |
| <span data-ttu-id="d5227-126">**mapcolor**</span><span class="sxs-lookup"><span data-stu-id="d5227-126">**mapcolor**</span></span>                      |                                                                                                                                               |                                                      |
| <span data-ttu-id="d5227-127">**RGBcolor**</span><span class="sxs-lookup"><span data-stu-id="d5227-127">**RGBcolor**</span></span>                      | <span data-ttu-id="d5227-128">**glColor**</span><span class="sxs-lookup"><span data-stu-id="d5227-128">**glColor**</span></span>                                                                                                                                   | <span data-ttu-id="d5227-129">Define a cor RGB.</span><span class="sxs-lookup"><span data-stu-id="d5227-129">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="d5227-130">**writemask**</span><span class="sxs-lookup"><span data-stu-id="d5227-130">**writemask**</span></span>                     | [<span data-ttu-id="d5227-131">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="d5227-131">**glIndexMask**</span></span>](glindexmask.md)                                                                                                            | <span data-ttu-id="d5227-132">Define a máscara de cor do modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="d5227-132">Sets the color-index mode color mask.</span></span>                |
| <span data-ttu-id="d5227-133">**wmpackRGBwritemask**</span><span class="sxs-lookup"><span data-stu-id="d5227-133">**wmpackRGBwritemask**</span></span><br/> | [<span data-ttu-id="d5227-134">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="d5227-134">**glColorMask**</span></span>](glcolormask.md)                                                                                                            | <span data-ttu-id="d5227-135">Define a máscara do modo de cor RGB.</span><span class="sxs-lookup"><span data-stu-id="d5227-135">Sets the RGB color mode mask.</span></span>                        |
| <span data-ttu-id="d5227-136">**getwritemask**</span><span class="sxs-lookup"><span data-stu-id="d5227-136">**getwritemask**</span></span>                  | <span data-ttu-id="d5227-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ Color \_ WRITEMASK)**glGet**( \_ índice GL \_ WRITEMASK)</span><span class="sxs-lookup"><span data-stu-id="d5227-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_COLOR\_WRITEMASK )**glGet**( GL\_INDEX\_WRITEMASK )</span></span><br/> | <span data-ttu-id="d5227-138">Obtém a máscara de cor.</span><span class="sxs-lookup"><span data-stu-id="d5227-138">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="d5227-139">**gRGBmask**</span><span class="sxs-lookup"><span data-stu-id="d5227-139">**gRGBmask**</span></span>                      | <span data-ttu-id="d5227-140">**glGet**(GL de \_ cor \_ WRITEMASK)</span><span class="sxs-lookup"><span data-stu-id="d5227-140">**glGet**( GL\_COLOR\_WRITEMASK )</span></span>                                                                                                             | <span data-ttu-id="d5227-141">Obtém a máscara de cor.</span><span class="sxs-lookup"><span data-stu-id="d5227-141">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="d5227-142">**zwritemask**</span><span class="sxs-lookup"><span data-stu-id="d5227-142">**zwritemask**</span></span>                    | [<span data-ttu-id="d5227-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="d5227-143">**glDepthMask**</span></span>](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> <span data-ttu-id="d5227-144">Tenha cuidado ao substituir **zwritemask** por [**glDepthMask**](gldepthmask.md); **glDepthMask** usa um argumento booliano, enquanto **zwritemask** usa um campo de bits.</span><span class="sxs-lookup"><span data-stu-id="d5227-144">Be careful when replacing **zwritemask** with [**glDepthMask**](gldepthmask.md); **glDepthMask** takes a Boolean argument, whereas **zwritemask** takes a bit field.</span></span>

 

<span data-ttu-id="d5227-145">Se você quiser usar vários mapas de cores, precisará usar as funções apropriadas do mapa de cores do Windows.</span><span class="sxs-lookup"><span data-stu-id="d5227-145">If you want to use multiple color maps, you need to use the appropriate Windows color map functions.</span></span> <span data-ttu-id="d5227-146">Portanto, **Multimap**, **onemap**, **getcmmode**, **Setmap** e **GetMap** não têm equivalentes OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d5227-146">Therefore, **multimap**, **onemap**, **getcmmode**, **setmap**, and **getmap** have no OpenGL equivalents.</span></span>

 

 





