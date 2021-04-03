---
title: Operação OpenGL básica
description: Operação OpenGL básica
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operações básicas
- OpenGL, processamento de dados
- OpenGL, estágios de processamento
- OpenGL, exibir listas
- Exibir listas OpenGL
- OpenGL, avaliadores
- avaliadores OpenGL
- OpenGL, operações por vértice
- operações por vértice OpenGL
- OpenGL, assembly primitivo
- assembly primitivo OpenGL
- OpenGL, rasterização
- OpenGL de rasterização
- OpenGL, operações por fragmento
- operações por fragmento OpenGL
- framebuffers, operações básicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930064"
---
# <a name="basic-opengl-operation"></a><span data-ttu-id="13967-119">Operação OpenGL básica</span><span class="sxs-lookup"><span data-stu-id="13967-119">Basic OpenGL Operation</span></span>

<span data-ttu-id="13967-120">O diagrama a seguir ilustra como o OpenGL processa os dados.</span><span class="sxs-lookup"><span data-stu-id="13967-120">The following diagram illustrates how OpenGL processes data.</span></span> <span data-ttu-id="13967-121">Conforme mostrado, os comandos entram da esquerda e passam por um pipeline de processamento.</span><span class="sxs-lookup"><span data-stu-id="13967-121">As shown, commands enter from the left and proceed through a processing pipeline.</span></span> <span data-ttu-id="13967-122">Alguns comandos especificam objetos geométricos a serem desenhados e outros controlam como os objetos são tratados durante vários estágios de processamento.</span><span class="sxs-lookup"><span data-stu-id="13967-122">Some commands specify geometric objects to be drawn, and others control how the objects are handled during various processing stages.</span></span>

![Diagrama mostrando os estágios do pipeline de processamento de dados OpenGL.](images/basic01.png)

<span data-ttu-id="13967-124">Os estágios de processamento na operação OpenGL básica são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="13967-124">The processing stages in basic OpenGL operation are as follows:</span></span>

-   <span data-ttu-id="13967-125">**Lista de exibição** Em vez de fazer com que todos os comandos continuem imediatamente por meio do pipeline, você pode optar por acumular alguns deles em uma lista de exibição para processamento posterior.</span><span class="sxs-lookup"><span data-stu-id="13967-125">**Display list** Rather than having all commands proceed immediately through the pipeline, you can choose to accumulate some of them in a display list for processing later.</span></span>
-   <span data-ttu-id="13967-126">**Avaliador** O estágio de processamento do avaliador fornece uma maneira eficiente de aproximar a curva e a geometria da superfície avaliando comandos polinomiais de valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="13967-126">**Evaluator** The evaluator stage of processing provides an efficient way to approximate curve and surface geometry by evaluating polynomial commands of input values.</span></span>
-   <span data-ttu-id="13967-127">**Operações por vértice e assembly primitivo** O OpenGL processa primitivespointss geométricos, segmentos de linha e polygonsall dos quais são descritos por vértices.</span><span class="sxs-lookup"><span data-stu-id="13967-127">**Per-vertex operations and primitive assembly** OpenGL processes geometric primitivespoints, line segments, and polygonsall of which are described by vertices.</span></span> <span data-ttu-id="13967-128">Os vértices são transformados e acesos e os primitivos são recortados para o visor na preparação para a rasterização.</span><span class="sxs-lookup"><span data-stu-id="13967-128">Vertices are transformed and lit, and primitives are clipped to the viewport in preparation for rasterization.</span></span>
-   <span data-ttu-id="13967-129">**Rasterização** O estágio de rasterização produz uma série de endereços de buffer de quadros e valores associados usando uma descrição bidimensional de um ponto, segmento de linha ou polígono.</span><span class="sxs-lookup"><span data-stu-id="13967-129">**Rasterization** The rasterization stage produces a series of frame-buffer addresses and associated values using a two-dimensional description of a point, line segment, or polygon.</span></span> <span data-ttu-id="13967-130">Cada fragmento produzido é colocado no último estágio por operações por fragmento.</span><span class="sxs-lookup"><span data-stu-id="13967-130">Each fragment so produced is fed into the last stage, per-fragment operations.</span></span>
-   <span data-ttu-id="13967-131">**Operações por fragmento** Essas são as operações finais executadas nos dados antes de serem armazenadas como pixels no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="13967-131">**Per-fragment operations** These are the final operations performed on the data before it is stored as pixels in the framebuffer.</span></span>

    <span data-ttu-id="13967-132">As operações por fragmento incluem atualizações condicionais para o framebuffer com base em valores z de entrada e armazenados anteriormente (para armazenamento em buffer z) e mesclagem de cores de pixel de entrada com cores armazenadas, bem como mascaramento e outras operações lógicas em valores de pixel.</span><span class="sxs-lookup"><span data-stu-id="13967-132">Per-fragment operations include conditional updates to the framebuffer based on incoming and previously stored z values (for z buffering) and blending of incoming pixel colors with stored colors, as well as masking and other logical operations on pixel values.</span></span>

<span data-ttu-id="13967-133">Os dados podem ser inseridos na forma de pixels em vez de vértices.</span><span class="sxs-lookup"><span data-stu-id="13967-133">Data can be input in the form of pixels rather than vertices.</span></span> <span data-ttu-id="13967-134">Dados na forma de pixels, como podem descrever uma imagem para uso no mapeamento de textura, ignora o primeiro estágio de processamento descrito acima e, em vez disso, é processado como pixels, no estágio de operações de pixel.</span><span class="sxs-lookup"><span data-stu-id="13967-134">Data in the form of pixels, such as might describe an image for use in texture mapping, skips the first stage of processing described above and instead is processed as pixels, in the pixel operations stage.</span></span> <span data-ttu-id="13967-135">Após as operações de pixel, os dados de pixel são:</span><span class="sxs-lookup"><span data-stu-id="13967-135">Following pixel operations, the pixel data is either:</span></span>

-   <span data-ttu-id="13967-136">Armazenado como memória de textura, para uso no estágio de rasterização.</span><span class="sxs-lookup"><span data-stu-id="13967-136">Stored as texture memory, for use in the rasterization stage.</span></span>
-   <span data-ttu-id="13967-137">Rasterizado, com os fragmentos resultantes mesclados no framebuffer como se fossem gerados a partir de dados geométricos.</span><span class="sxs-lookup"><span data-stu-id="13967-137">Rasterized, with the resulting fragments merged into the framebuffer just as if they were generated from geometric data.</span></span>

 

 




