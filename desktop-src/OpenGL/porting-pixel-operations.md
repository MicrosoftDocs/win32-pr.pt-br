---
title: Portando operações de pixel
description: Portando operações de pixel
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Portabilidade do íris GL, pixels
- portando do íris GL, pixels
- portando para OpenGL do íris GL, pixels
- Portabilidade do OpenGL do íris GL, pixels
- pixels, portando do íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636571"
---
# <a name="porting-pixel-operations"></a><span data-ttu-id="577e2-108">Portando operações de pixel</span><span class="sxs-lookup"><span data-stu-id="577e2-108">Porting Pixel Operations</span></span>

<span data-ttu-id="577e2-109">Ao portar o código que envolve operações de pixel, tenha em mente os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="577e2-109">When porting code that involves pixel operations, keep the following points in mind:</span></span>

-   <span data-ttu-id="577e2-110">As operações de pixel lógico não são aplicadas a buffers de cores RGBA.</span><span class="sxs-lookup"><span data-stu-id="577e2-110">Logical pixel operations are not applied to RGBA color buffers.</span></span> <span data-ttu-id="577e2-111">Para obter mais informações, consulte [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="577e2-111">For more information, see [**glLogicOp**](gllogicop.md).</span></span>
-   <span data-ttu-id="577e2-112">Em geral, a íris GL usa o formato ABGR para pixels, enquanto OpenGL usa RGBA.</span><span class="sxs-lookup"><span data-stu-id="577e2-112">In general, IRIS GL uses the format ABGR for pixels, whereas OpenGL uses RGBA.</span></span> <span data-ttu-id="577e2-113">Você pode alterar o formato com [**glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="577e2-113">You can change the format with [**glPixelStore**](glpixelstore-functions.md).</span></span>
-   <span data-ttu-id="577e2-114">Ao portar funções do **lrectwrite** , tenha cuidado para observar onde o **lrectwrite** está gravando (por exemplo, ele pode estar gravando no buffer de profundidade).</span><span class="sxs-lookup"><span data-stu-id="577e2-114">When porting **lrectwrite** functions, be careful to note where **lrectwrite** is writing (for example, it could be writing to the depth buffer).</span></span>

<span data-ttu-id="577e2-115">O OpenGL oferece mais flexibilidade em operações de pixel.</span><span class="sxs-lookup"><span data-stu-id="577e2-115">OpenGL gives you some additional flexibility in pixel operations.</span></span> <span data-ttu-id="577e2-116">A tabela a seguir lista as funções do íris GL para operações de pixel e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="577e2-116">The following table lists IRIS GL functions for pixel operations and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="577e2-117">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="577e2-117">IRIS GL function</span></span>                                   | <span data-ttu-id="577e2-118">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="577e2-118">OpenGL function</span></span>                                                                           | <span data-ttu-id="577e2-119">Significado</span><span class="sxs-lookup"><span data-stu-id="577e2-119">Meaning</span></span>                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="577e2-120">**lrectread**, **rectread**,**readRGB**</span><span class="sxs-lookup"><span data-stu-id="577e2-120">**lrectread**, **rectread**,**readRGB**</span></span><br/> | [<span data-ttu-id="577e2-121">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="577e2-121">**glReadPixels**</span></span>](glreadpixels.md)                                                      | <span data-ttu-id="577e2-122">Lê um bloco de pixels do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="577e2-122">Reads a block of pixels from the framebuffer.</span></span>                           |
| <span data-ttu-id="577e2-123">**lrectwrite**, **rectwrite**</span><span class="sxs-lookup"><span data-stu-id="577e2-123">**lrectwrite**, **rectwrite**</span></span>                      | [<span data-ttu-id="577e2-124">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="577e2-124">**glDrawPixels**</span></span>](gldrawpixels.md)                                                      | <span data-ttu-id="577e2-125">Grava um bloco de pixels no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="577e2-125">Writes a block of pixels to the framebuffer.</span></span>                            |
| <span data-ttu-id="577e2-126">**rectcopy**</span><span class="sxs-lookup"><span data-stu-id="577e2-126">**rectcopy**</span></span>                                       | [<span data-ttu-id="577e2-127">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="577e2-127">**glCopyPixels**</span></span>](glcopypixels.md)                                                      | <span data-ttu-id="577e2-128">Copia os pixels no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="577e2-128">Copies pixels in the framebuffer.</span></span>                                       |
| <span data-ttu-id="577e2-129">**rectzoom**</span><span class="sxs-lookup"><span data-stu-id="577e2-129">**rectzoom**</span></span>                                       | [<span data-ttu-id="577e2-130">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="577e2-130">**glPixelZoom**</span></span>](glpixelzoom.md)                                                        | <span data-ttu-id="577e2-131">Especifica fatores de zoom de pixel para **glDrawPixels** e **glCopyPixels**.</span><span class="sxs-lookup"><span data-stu-id="577e2-131">Specifies pixel zoom factors for **glDrawPixels** and **glCopyPixels**.</span></span> |
| <span data-ttu-id="577e2-132">**cmov**</span><span class="sxs-lookup"><span data-stu-id="577e2-132">**cmov**</span></span>                                           | [<span data-ttu-id="577e2-133">glRasterPos</span><span class="sxs-lookup"><span data-stu-id="577e2-133">glRasterPos</span></span>](glrasterpos-functions.md)                                                  | <span data-ttu-id="577e2-134">Especifica a posição da varredura para as operações de pixel.</span><span class="sxs-lookup"><span data-stu-id="577e2-134">Specifies raster position for pixel operations.</span></span>                         |
| <span data-ttu-id="577e2-135">**leitura**</span><span class="sxs-lookup"><span data-stu-id="577e2-135">**readsource**</span></span>                                     | [<span data-ttu-id="577e2-136">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="577e2-136">**glReadBuffer**</span></span>](glreadbuffer.md)                                                      | <span data-ttu-id="577e2-137">Seleciona uma fonte de buffer de cores para pixels.</span><span class="sxs-lookup"><span data-stu-id="577e2-137">Selects a color buffer source for pixels.</span></span>                               |
| <span data-ttu-id="577e2-138">**pixmode**</span><span class="sxs-lookup"><span data-stu-id="577e2-138">**pixmode**</span></span>                                        | <span data-ttu-id="577e2-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span><span class="sxs-lookup"><span data-stu-id="577e2-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span></span> | <span data-ttu-id="577e2-140">Define os modos de armazenamento em pixels. Definir modos de transferência de pixel.</span><span class="sxs-lookup"><span data-stu-id="577e2-140">Sets pixel storage modes.Set pixel transfer modes.</span></span>                      |
| <span data-ttu-id="577e2-141">**logicop**</span><span class="sxs-lookup"><span data-stu-id="577e2-141">**logicop**</span></span>                                        | [<span data-ttu-id="577e2-142">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="577e2-142">**glLogicOp**</span></span>](gllogicop.md)                                                            | <span data-ttu-id="577e2-143">Especifica uma operação lógica para gravações de pixel.</span><span class="sxs-lookup"><span data-stu-id="577e2-143">Specifies a logical operation for pixel writes.</span></span>                         |
|                                                    | <span data-ttu-id="577e2-144">[**glEnable**](glenable.md) ( \_ op lógico GL \_ )</span><span class="sxs-lookup"><span data-stu-id="577e2-144">[**glEnable**](glenable.md) ( GL\_LOGIC\_OP )</span></span>                                            | <span data-ttu-id="577e2-145">Ativa operações lógicas de pixel.</span><span class="sxs-lookup"><span data-stu-id="577e2-145">Turns on pixel logic operations.</span></span>                                        |



 

<span data-ttu-id="577e2-146">Para obter uma lista completa de possíveis operações lógicas, consulte [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="577e2-146">For a complete list of possible logical operations, see [**glLogicOp**](gllogicop.md).</span></span>

<span data-ttu-id="577e2-147">Este exemplo de código do íris GL mostra uma gravação de pixel típica:</span><span class="sxs-lookup"><span data-stu-id="577e2-147">This IRIS GL code sample shows a typical pixel write:</span></span>

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

<span data-ttu-id="577e2-148">O código anterior tem esta aparência quando traduzido para OpenGL:</span><span class="sxs-lookup"><span data-stu-id="577e2-148">The preceding code looks like this when translated to OpenGL:</span></span>

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





