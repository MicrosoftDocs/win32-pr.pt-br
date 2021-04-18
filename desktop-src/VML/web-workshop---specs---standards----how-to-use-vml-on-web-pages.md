---
title: Como usar o VML em páginas da Web
description: Como usar o VML em páginas da Web
ms.assetid: ae20b789-1890-4560-bcc0-536f126c5a41
keywords:
- Linguagem VML (VML), Web Workshop
- VML (linguagem VML), Web Workshop
- gráficos vetoriais, Web Workshop
- Linguagem VML (VML), criando páginas da Web
- VML (linguagem VML), criando páginas da Web
- gráficos vetoriais, criação de páginas da Web
- Criando páginas da Web, tarefas de VML
- Web Workshop, tarefas de VML
- Criando páginas da Web, linguagem VML (VML)
- Web Workshop, linguagem VML (VML)
- Linguagem VML (VML), World Wide Web Consortium (W3C)
- VML (linguagem VML), World Wide Web Consortium (W3C)
- gráficos vetoriais, World Wide Web Consortium (W3C)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189353fd5a6c50ffbdcf3fe2ad3efe7e82b8e219
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105766346"
---
# <a name="how-to-use-vml-on-webpages"></a><span data-ttu-id="37025-116">Como usar o VML em páginas da Web</span><span class="sxs-lookup"><span data-stu-id="37025-116">How to Use VML on Webpages</span></span>

<span data-ttu-id="37025-117">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="37025-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="37025-118">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="37025-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="37025-119">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="37025-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="37025-120">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="37025-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="37025-121">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="37025-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="37025-122">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="37025-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="37025-123">Este documento complementa a [especificação de linguagem VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) que foi enviada para o World Wide Web CONSORTIUM (W3C).</span><span class="sxs-lookup"><span data-stu-id="37025-123">This document supplements the [Vector Markup Language (VML) specification](https://www.w3.org/TR/NOTE-datetime.html) that was submitted to the World Wide Web Consortium (W3C).</span></span> <span data-ttu-id="37025-124">Com este documento e a especificação de VML completa, você deve ser capaz de usar o VML para criar páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="37025-124">With this document and the complete VML specification, you should be able to use VML to design webpages.</span></span> <span data-ttu-id="37025-125">Supomos que você já tem um conhecimento funcional do HTML.</span><span class="sxs-lookup"><span data-stu-id="37025-125">We have assumed that you already have a working knowledge of HTML.</span></span>

## <a name="part-i-basic-topics"></a><span data-ttu-id="37025-126">Parte I: tópicos básicos</span><span class="sxs-lookup"><span data-stu-id="37025-126">Part I: Basic Topics</span></span>

-   [<span data-ttu-id="37025-127">Formas básicas de desenho</span><span class="sxs-lookup"><span data-stu-id="37025-127">Drawing Basic Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----drawing-basic-shapes.md)
-   [<span data-ttu-id="37025-128">Usando formas predefinidas</span><span class="sxs-lookup"><span data-stu-id="37025-128">Using Predefined Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----using-predefined-shapes.md)
-   [<span data-ttu-id="37025-129">Formas de cores</span><span class="sxs-lookup"><span data-stu-id="37025-129">Coloring Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----coloring-shapes.md)
-   [<span data-ttu-id="37025-130">Dimensionando formas</span><span class="sxs-lookup"><span data-stu-id="37025-130">Scaling Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md)
-   [<span data-ttu-id="37025-131">Posicionando formas</span><span class="sxs-lookup"><span data-stu-id="37025-131">Positioning Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----positioning-shapes.md)
-   [<span data-ttu-id="37025-132">Agrupando formas</span><span class="sxs-lookup"><span data-stu-id="37025-132">Grouping Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----grouping-shapes.md)

## <a name="part-ii-advanced-topics"></a><span data-ttu-id="37025-133">Parte II: Tópicos avançados</span><span class="sxs-lookup"><span data-stu-id="37025-133">Part II: Advanced Topics</span></span>

-   [<span data-ttu-id="37025-134">Usando o elemento ShapeType</span><span class="sxs-lookup"><span data-stu-id="37025-134">Using the Shapetype Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----shapetype--element.md)
-   [<span data-ttu-id="37025-135">Usando o elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="37025-135">Using the Stroke Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----stroke--element.md)
-   [<span data-ttu-id="37025-136">Usar o elemento Fill</span><span class="sxs-lookup"><span data-stu-id="37025-136">Using the Fill Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)
-   [<span data-ttu-id="37025-137">Usando o elemento Image</span><span class="sxs-lookup"><span data-stu-id="37025-137">Using the Image Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----image--element.md)
-   [<span data-ttu-id="37025-138">Usando o elemento background</span><span class="sxs-lookup"><span data-stu-id="37025-138">Using the Background Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----background--element.md)
-   [<span data-ttu-id="37025-139">Usando o elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="37025-139">Using the Shadow Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----shadow--element.md)
-   [<span data-ttu-id="37025-140">Usando o elemento Path</span><span class="sxs-lookup"><span data-stu-id="37025-140">Using the Path Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----path--element.md)
-   [<span data-ttu-id="37025-141">Usando o elemento TextBox</span><span class="sxs-lookup"><span data-stu-id="37025-141">Using the Textbox Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----textbox--element.md)
-   [<span data-ttu-id="37025-142">Usando o espaço de coordenadas local</span><span class="sxs-lookup"><span data-stu-id="37025-142">Using Local Coordinate Space</span></span>](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md)
-   [<span data-ttu-id="37025-143">Usando o elemento fórmulas</span><span class="sxs-lookup"><span data-stu-id="37025-143">Using the Formulas Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----formulas--element.md)
-   [<span data-ttu-id="37025-144">Usando o elemento Handles</span><span class="sxs-lookup"><span data-stu-id="37025-144">Using the Handles Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----handles--element.md)
-   [<span data-ttu-id="37025-145">Usando o elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="37025-145">Using the Textpath Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----textpath--element.md)

> [!Note]  
> <span data-ttu-id="37025-146">Os exemplos fornecidos nesta referência foram projetados para o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="37025-146">The samples provided in this reference are designed for Internet Explorer.</span></span> <span data-ttu-id="37025-147">Também fornecemos ilustrações sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="37025-147">We have also provided illustrations where possible.</span></span>

 

 

 