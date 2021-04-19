---
title: Por que usar DirectComposition
description: Este tópico descreve os recursos e os benefícios do Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Por que usar DirectComposition
- motivos para usar o DirectComposition
- Recursos e benefícios do DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810620"
---
# <a name="why-use-directcomposition"></a><span data-ttu-id="3c858-106">Por que usar o DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="3c858-106">Why use DirectComposition?</span></span>

> [!NOTE]
> <span data-ttu-id="3c858-107">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3c858-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="3c858-108">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="3c858-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="3c858-109">Este tópico descreve os recursos e os benefícios do Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3c858-109">This topic describes the capabilities and benefits of Microsoft DirectComposition.</span></span> <span data-ttu-id="3c858-110">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="3c858-110">It contains the following sections:</span></span>

-   [<span data-ttu-id="3c858-111">Criar uma interface do usuário visualmente atraente</span><span class="sxs-lookup"><span data-stu-id="3c858-111">Create a visually engaging user interface</span></span>](#create-a-visually-engaging-user-interface)
-   [<span data-ttu-id="3c858-112">Habilite animações avançadas e suaves para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="3c858-112">Enable rich, smooth animations for your application</span></span>](#enable-rich-smooth-animations-for-your-application)
-   [<span data-ttu-id="3c858-113">Combinar bitmaps de uma variedade de fontes</span><span class="sxs-lookup"><span data-stu-id="3c858-113">Combine bitmaps from a variety of sources</span></span>](#combine-bitmaps-from-a-variety-of-sources)
-   [<span data-ttu-id="3c858-114">Economia de memória por meio da integração com o DWM</span><span class="sxs-lookup"><span data-stu-id="3c858-114">Memory savings though integration with DWM</span></span>](#memory-savings-though-integration-with-dwm)
-   [<span data-ttu-id="3c858-115">Mantenha o que você já tem</span><span class="sxs-lookup"><span data-stu-id="3c858-115">Keep what you already have</span></span>](#keep-what-you-already-have)
-   [<span data-ttu-id="3c858-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c858-116">Related topics</span></span>](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a><span data-ttu-id="3c858-117">Criar uma interface do usuário visualmente atraente</span><span class="sxs-lookup"><span data-stu-id="3c858-117">Create a visually engaging user interface</span></span>

<span data-ttu-id="3c858-118">O DirectComposition permite combinar e animar [*visuais*](directcomposition-glossary.md) para criar uma interface do usuário visualmente envolvente para seus aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="3c858-118">DirectComposition lets you combine and animate [*visuals*](directcomposition-glossary.md) to create a visually engaging UI for your Windows-based applications.</span></span> <span data-ttu-id="3c858-119">Ele pode ajudar a dar uma aparência única ao seu aplicativo, estabelecendo uma identidade que o define de forma separada de outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3c858-119">It can help give your application a unique look and feel, establishing an identity that sets it apart from other applications.</span></span>

<span data-ttu-id="3c858-120">O DirectComposition também pode ajudar a facilitar o uso de seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3c858-120">DirectComposition can also help make your applications easier to use.</span></span> <span data-ttu-id="3c858-121">Por exemplo, você pode usar isso para criar indicações visuais e transições de tela animadas que mostram as relações entre os itens na tela.</span><span class="sxs-lookup"><span data-stu-id="3c858-121">For example, you can use it to create visual cues and animated screen transitions that show relationships among items on the screen.</span></span>

## <a name="enable-rich-smooth-animations-for-your-application"></a><span data-ttu-id="3c858-122">Habilite animações avançadas e suaves para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="3c858-122">Enable rich, smooth animations for your application</span></span>

<span data-ttu-id="3c858-123">DirectComposition é um mecanismo de composição de bitmap de alto desempenho que usa gráficos acelerados por hardware para atingir altas taxas de quadros, resultando em visão panorâmica, rolagem e animações de conteúdo complexo.</span><span class="sxs-lookup"><span data-stu-id="3c858-123">DirectComposition is a high-performance bitmap composition engine that uses hardware-accelerated graphics to achieve high frame rates, resulting in smooth and consistent panning, scrolling, and animations of complex content.</span></span> <span data-ttu-id="3c858-124">Como ele opera em um thread dedicado que é separado do thread usado para renderizar a interface do usuário do aplicativo, o DirectComposition nunca pode "privar" o thread da interface do usuário ou interferir na capacidade do aplicativo de desenhar seus elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3c858-124">Because it operates on a dedicated thread that is separate from the thread used to render the application UI, DirectComposition can never "starve" the UI thread or interfere with the application's ability to draw its UI elements.</span></span>

## <a name="combine-bitmaps-from-a-variety-of-sources"></a><span data-ttu-id="3c858-125">Combinar bitmaps de uma variedade de fontes</span><span class="sxs-lookup"><span data-stu-id="3c858-125">Combine bitmaps from a variety of sources</span></span>

<span data-ttu-id="3c858-126">Muitos aplicativos baseados no Windows têm uma interface do usuário que consiste em elementos criados por uma variedade de estruturas gráficas diferentes.</span><span class="sxs-lookup"><span data-stu-id="3c858-126">Many Windows-based applications have a UI that consists of elements created by a variety of different graphics frameworks.</span></span> <span data-ttu-id="3c858-127">Por exemplo, um aplicativo pode usar Windows Forms para criar uma barra de status, o Windows Graphics Device Interface (GDI) para criar o conteúdo da janela principal, o Microsoft DirectX para conteúdo de gráficos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3c858-127">For example, an application might use Windows Forms to create a status bar, Windows Graphics Device Interface (GDI) to create the main window content, Microsoft DirectX for graphics content, and so on.</span></span> <span data-ttu-id="3c858-128">O DirectComposition permite combinar o conteúdo de uma variedade de estruturas gráficas e fazer com que ela seja processada para a mesma janela de nível superior ou filho sem a necessidade de se preocupar com o que acontece se o conteúdo de diferentes estruturas se sobrepuser.</span><span class="sxs-lookup"><span data-stu-id="3c858-128">DirectComposition enables you to combine the content from a variety of graphics frameworks and have it render to the same top-level or child window without needing to worry about what happens if the content from different frameworks overlaps.</span></span>

## <a name="memory-savings-though-integration-with-dwm"></a><span data-ttu-id="3c858-129">Economia de memória por meio da integração com o DWM</span><span class="sxs-lookup"><span data-stu-id="3c858-129">Memory savings though integration with DWM</span></span>

<span data-ttu-id="3c858-130">Composições e animações criadas por DirectComposition são passadas para um componente interno do Windows chamado [Gerenciador de janelas da área de trabalho (DWM)](/windows/desktop/dwm/dwm-overview) para renderização na tela.</span><span class="sxs-lookup"><span data-stu-id="3c858-130">Compositions and animations created by DirectComposition are passed to a built-in component of Windows called [Desktop Window Manager (DWM)](/windows/desktop/dwm/dwm-overview) for rendering to the screen.</span></span> <span data-ttu-id="3c858-131">Portanto, nenhum componente de renderização especial ou estruturas de interface do usuário são necessários no computador.</span><span class="sxs-lookup"><span data-stu-id="3c858-131">Therefore, no special rendering components or UI frameworks are required on the computer.</span></span>

## <a name="keep-what-you-already-have"></a><span data-ttu-id="3c858-132">Mantenha o que você já tem</span><span class="sxs-lookup"><span data-stu-id="3c858-132">Keep what you already have</span></span>

<span data-ttu-id="3c858-133">O código da interface do usuário em um aplicativo existente baseado no Windows representa um investimento significativo.</span><span class="sxs-lookup"><span data-stu-id="3c858-133">The UI code in an existing Windows-based application represents a significant investment.</span></span> <span data-ttu-id="3c858-134">Para a maior parte, o DirectComposition permite compor e animar o conteúdo da interface do usuário existente.</span><span class="sxs-lookup"><span data-stu-id="3c858-134">For the most part, DirectComposition lets you compose and animate your existing UI content.</span></span> <span data-ttu-id="3c858-135">Isso significa que você pode usar o DirectComposition para fazer atualizações e aprimoramentos significativos na interface do usuário do aplicativo sem a necessidade de fazer alterações extensivas na base de código da interface do usuário existente.</span><span class="sxs-lookup"><span data-stu-id="3c858-135">This means you can use DirectComposition to make significant updates and enhancements to your application UI without needing to make extensive changes to your existing UI code base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c858-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c858-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c858-137">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3c858-137">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 