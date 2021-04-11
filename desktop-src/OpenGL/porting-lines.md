---
title: Linhas de porta
description: Portar código GL do íris que desenha linhas é razoavelmente simples, embora você deva observar as diferenças no modo OpenGL stipples. A tabela a seguir lista as funções da íris GL para desenhar linhas e suas funções OpenGL equivalentes.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Portabilidade do íris GL, linhas
- portando do íris GL, linhas
- portando para OpenGL do íris GL, linhas
- Portabilidade OpenGL do íris GL, linhas
- funções de desenho, linhas
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160204"
---
# <a name="porting-lines"></a><span data-ttu-id="3dcf6-110">Linhas de porta</span><span class="sxs-lookup"><span data-stu-id="3dcf6-110">Porting Lines</span></span>

<span data-ttu-id="3dcf6-111">Portar código GL do íris que desenha linhas é razoavelmente simples, embora você deva observar as diferenças no modo OpenGL stipples.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-111">Porting IRIS GL code that draws lines is fairly straightforward, though you should note the differences in the way OpenGL stipples.</span></span> <span data-ttu-id="3dcf6-112">A tabela a seguir lista as funções da íris GL para desenhar linhas e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-112">The following table lists IRIS GL functions for drawing lines and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="3dcf6-113">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="3dcf6-113">IRIS GL function</span></span>                               | <span data-ttu-id="3dcf6-114">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="3dcf6-114">OpenGL function</span></span>                                                                                         | <span data-ttu-id="3dcf6-115">Significado</span><span class="sxs-lookup"><span data-stu-id="3dcf6-115">Meaning</span></span>                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcf6-116">**bgnclosedline**,**preclosed**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-116">**bgnclosedline**,**endclosedline**</span></span><br/> | <span data-ttu-id="3dcf6-117">[**glBegin**](glbegin.md) ( \_ loop de linha gl \_ )[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="3dcf6-117">[**glBegin**](glbegin.md) ( GL\_LINE\_LOOP )[**glEnd**](glend.md)</span></span><br/>                          | <span data-ttu-id="3dcf6-118">Desenha uma linha fechada.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-118">Draws a closed line.</span></span>                                                                                                                         |
| <span data-ttu-id="3dcf6-119">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-119">**bgnline**</span></span>                                    | <span data-ttu-id="3dcf6-120">[**glBegin**](glbegin.md) ( \_ faixa de linha gl \_ )</span><span class="sxs-lookup"><span data-stu-id="3dcf6-120">[**glBegin**](glbegin.md) ( GL\_LINE\_STRIP )</span></span>                                                          | <span data-ttu-id="3dcf6-121">Desenha segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-121">Draws line segments.</span></span>                                                                                                                         |
| <span data-ttu-id="3dcf6-122">**linewidth**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-122">**linewidth**</span></span>                                  | [<span data-ttu-id="3dcf6-123">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-123">**glLineWidth**</span></span>](gllinewidth.md)                                                                      | <span data-ttu-id="3dcf6-124">Define a largura da linha.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-124">Sets line width.</span></span>                                                                                                                             |
| <span data-ttu-id="3dcf6-125">**getlwidth**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-125">**getlwidth**</span></span>                                  | <span data-ttu-id="3dcf6-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ largura da linha gl \_ )</span><span class="sxs-lookup"><span data-stu-id="3dcf6-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_WIDTH )</span></span>            | <span data-ttu-id="3dcf6-127">Retorna a largura da linha atual.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-127">Returns current line width.</span></span>                                                                                                                  |
| <span data-ttu-id="3dcf6-128">**deflinestyle**,**setlinestyle**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-128">**deflinestyle**,**setlinestyle**</span></span><br/>   | [<span data-ttu-id="3dcf6-129">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-129">**glLineStipple**</span></span>](gllinestipple.md)                                                                  | <span data-ttu-id="3dcf6-130">Especifica um padrão de Stipple de linha.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-130">Specifies a line stipple pattern.</span></span>                                                                                                            |
| <span data-ttu-id="3dcf6-131">**lsrepeat**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-131">**lsrepeat**</span></span>                                   | <span data-ttu-id="3dcf6-132">argumento de fator de **glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-132">factor argument of **glLineStipple**</span></span>                                                                    | <span data-ttu-id="3dcf6-133">Define um fator de repetição para o estilo de linha.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-133">Sets a repeat factor for the line style.</span></span>                                                                                                     |
| <span data-ttu-id="3dcf6-134">**getlstyle**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-134">**getlstyle**</span></span>                                  | <span data-ttu-id="3dcf6-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ padrão de linha gl \_ STIPPLE \_ )</span><span class="sxs-lookup"><span data-stu-id="3dcf6-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_PATTERN )</span></span> | <span data-ttu-id="3dcf6-136">Retorna o padrão de Stipple de linha.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-136">Returns line stipple pattern.</span></span>                                                                                                                |
| <span data-ttu-id="3dcf6-137">**getlsrepeat**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-137">**getlsrepeat**</span></span>                                | <span data-ttu-id="3dcf6-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ STIPPLE de linha gl \_ \_ repetir)</span><span class="sxs-lookup"><span data-stu-id="3dcf6-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_REPEAT )</span></span>  | <span data-ttu-id="3dcf6-139">Retorna o fator de repetição.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-139">Returns repeat factor.</span></span>                                                                                                                       |
| <span data-ttu-id="3dcf6-140">**linesmooth**, **suavização**</span><span class="sxs-lookup"><span data-stu-id="3dcf6-140">**linesmooth**, **smoothline**</span></span>                 | <span data-ttu-id="3dcf6-141">[**glEnable**](glenable.md) ( \_ linha simples de GL \_ )</span><span class="sxs-lookup"><span data-stu-id="3dcf6-141">[**glEnable**](glenable.md) ( GL\_LINE\_SMOOTH )</span></span>                                                       | <span data-ttu-id="3dcf6-142">Ativa a suavização de linha (para obter mais informações sobre a anti-aliasing, consulte [portando funções de anti-aliasing](porting-antialiasing-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="3dcf6-142">Turns on line antialiasing (For more information on antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="3dcf6-143">O OpenGL não usa tabelas para a linha stipples; Ele mantém apenas um padrão Stipple de linha.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-143">OpenGL doesn't use tables for line stipples; it maintains only one line-stipple pattern.</span></span> <span data-ttu-id="3dcf6-144">Você pode usar [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) para alternar entre diferentes padrões de Stipple.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-144">You can use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to switch between different stipple patterns.</span></span>

<span data-ttu-id="3dcf6-145">Funções de estilo de linha mais antigas do íris GL (como **draw**, **lsbackup**, **getlsbackup** e assim por diante) não são suportadas por OpenGL.</span><span class="sxs-lookup"><span data-stu-id="3dcf6-145">Older IRIS GL line style functions (such as **draw**, **lsbackup**, **getlsbackup**, and so on) are not supported by OpenGL.</span></span>

<span data-ttu-id="3dcf6-146">Para obter informações sobre como desenhar linhas AntiAlias, consulte [portando funções de anti-aliasing](porting-antialiasing-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3dcf6-146">For information on drawing antialiased lines, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).</span></span>

<span data-ttu-id="3dcf6-147">??</span><span class="sxs-lookup"><span data-stu-id="3dcf6-147">??</span></span>

 

 





