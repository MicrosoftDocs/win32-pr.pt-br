---
description: A interface de dispositivo gráfico do Microsoft Windows (GDI) permite que os aplicativos usem gráficos e texto formatado na tela de vídeo e na impressora.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: GDI do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5fc6ba9f4eb99786b21daeff2e1c48b9ce09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967852"
---
# <a name="windows-gdi"></a><span data-ttu-id="58e98-103">GDI do Windows</span><span class="sxs-lookup"><span data-stu-id="58e98-103">Windows GDI</span></span>

## <a name="purpose"></a><span data-ttu-id="58e98-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="58e98-104">Purpose</span></span>

<span data-ttu-id="58e98-105">A interface de dispositivo gráfico do Microsoft Windows (GDI) permite que os aplicativos usem gráficos e texto formatado na tela de vídeo e na impressora.</span><span class="sxs-lookup"><span data-stu-id="58e98-105">The Microsoft Windows graphics device interface (GDI) enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="58e98-106">Os aplicativos baseados no Windows não acessam diretamente o hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="58e98-106">Windows-based applications do not access the graphics hardware directly.</span></span> <span data-ttu-id="58e98-107">Em vez disso, a GDI interage com drivers de dispositivo em nome dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="58e98-107">Instead, GDI interacts with device drivers on behalf of applications.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="58e98-108">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="58e98-108">Where applicable</span></span>

<span data-ttu-id="58e98-109">O GDI pode ser usado em todos os aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="58e98-109">GDI can be used in all Windows-based applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="58e98-110">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="58e98-110">Developer audience</span></span>

<span data-ttu-id="58e98-111">Essa API foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="58e98-111">This API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="58e98-112">É necessário ter familiaridade com a [arquitetura orientada a mensagens](../learnwin32/window-messages.md) do Windows.</span><span class="sxs-lookup"><span data-stu-id="58e98-112">Familiarity with the Windows [message-driven architecture](../learnwin32/window-messages.md) is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="58e98-113">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="58e98-113">Run-time requirements</span></span>

<span data-ttu-id="58e98-114">Para obter informações sobre quais sistemas operacionais são necessários para usar uma função específica, consulte a seção requisitos da documentação da função.</span><span class="sxs-lookup"><span data-stu-id="58e98-114">For information on which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58e98-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="58e98-115">In this section</span></span>

-   [<span data-ttu-id="58e98-116">Bitmaps</span><span class="sxs-lookup"><span data-stu-id="58e98-116">Bitmaps</span></span>](bitmaps.md)
-   [<span data-ttu-id="58e98-117">Pincéis</span><span class="sxs-lookup"><span data-stu-id="58e98-117">Brushes</span></span>](brushes.md)
-   [<span data-ttu-id="58e98-118">Recorte</span><span class="sxs-lookup"><span data-stu-id="58e98-118">Clipping</span></span>](clipping.md)
-   [<span data-ttu-id="58e98-119">Cores</span><span class="sxs-lookup"><span data-stu-id="58e98-119">Colors</span></span>](colors.md)
-   [<span data-ttu-id="58e98-120">Coordenar espaços e transformações</span><span class="sxs-lookup"><span data-stu-id="58e98-120">Coordinate Spaces and Transformations</span></span>](coordinate-spaces-and-transformations.md)
-   [<span data-ttu-id="58e98-121">Contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="58e98-121">Device Contexts</span></span>](device-contexts.md)
-   [<span data-ttu-id="58e98-122">Formas preenchidas</span><span class="sxs-lookup"><span data-stu-id="58e98-122">Filled Shapes</span></span>](filled-shapes.md)
-   [<span data-ttu-id="58e98-123">Fontes e texto</span><span class="sxs-lookup"><span data-stu-id="58e98-123">Fonts and Text</span></span>](fonts-and-text.md)
-   [<span data-ttu-id="58e98-124">Linhas e curvas</span><span class="sxs-lookup"><span data-stu-id="58e98-124">Lines and Curves</span></span>](lines-and-curves.md)
-   [<span data-ttu-id="58e98-125">Metarquivos</span><span class="sxs-lookup"><span data-stu-id="58e98-125">Metafiles</span></span>](metafiles.md)
-   [<span data-ttu-id="58e98-126">Vários monitores de exibição</span><span class="sxs-lookup"><span data-stu-id="58e98-126">Multiple Display Monitors</span></span>](multiple-display-monitors.md)
-   [<span data-ttu-id="58e98-127">Pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="58e98-127">Painting and Drawing</span></span>](painting-and-drawing.md)
-   [<span data-ttu-id="58e98-128">Caminhos</span><span class="sxs-lookup"><span data-stu-id="58e98-128">Paths</span></span>](paths.md)
-   [<span data-ttu-id="58e98-129">Canetas</span><span class="sxs-lookup"><span data-stu-id="58e98-129">Pens</span></span>](pens.md)
-   <span data-ttu-id="58e98-130">[Spooler de impressão e impressão](/previous-versions//dd162860(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58e98-130">[Printing and Print Spooler](/previous-versions//dd162860(v=vs.85))</span></span>
-   [<span data-ttu-id="58e98-131">Retângulos</span><span class="sxs-lookup"><span data-stu-id="58e98-131">Rectangles</span></span>](rectangles.md)
-   [<span data-ttu-id="58e98-132">Regiões</span><span class="sxs-lookup"><span data-stu-id="58e98-132">Regions</span></span>](regions.md)

## <a name="related-topics"></a><span data-ttu-id="58e98-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58e98-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58e98-134">DirectX</span><span class="sxs-lookup"><span data-stu-id="58e98-134">DirectX</span></span>](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[<span data-ttu-id="58e98-135">GDI+</span><span class="sxs-lookup"><span data-stu-id="58e98-135">GDI+</span></span>](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[<span data-ttu-id="58e98-136">OpenGL</span><span class="sxs-lookup"><span data-stu-id="58e98-136">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="58e98-137">Aquisição de imagem do Windows</span><span class="sxs-lookup"><span data-stu-id="58e98-137">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> </dl>

 

 
