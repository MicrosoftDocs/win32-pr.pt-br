---
title: Glossário do DirectComposition
description: Este tópico define os termos do Microsoft DirectComposition.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294203"
---
# <a name="directcomposition-glossary"></a><span data-ttu-id="94725-103">Glossário do DirectComposition</span><span class="sxs-lookup"><span data-stu-id="94725-103">DirectComposition glossary</span></span>

> [!NOTE]
> <span data-ttu-id="94725-104">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="94725-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="94725-105">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="94725-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="94725-106">Este tópico define os termos do Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="94725-106">This topic defines Microsoft DirectComposition terms.</span></span>

<dl> <dt>

<span data-ttu-id="94725-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**função de animação**</span><span class="sxs-lookup"><span data-stu-id="94725-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animation function**</span></span>
</dt> <dd>

<span data-ttu-id="94725-108">Uma construção que especifica como o valor de uma única propriedade de objeto é alterado ao longo de um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="94725-108">A construct that specifies how the value of a single object property changes over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="94725-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**objeto de animação**</span><span class="sxs-lookup"><span data-stu-id="94725-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**animation object**</span></span>
</dt> <dd>

<span data-ttu-id="94725-110">Um objeto que representa uma função para animar as propriedades de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="94725-110">An object that represents a function for animating the properties of another object.</span></span>

</dd> <dt>

<span data-ttu-id="94725-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segmento de animação**</span><span class="sxs-lookup"><span data-stu-id="94725-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**animation segment**</span></span>
</dt> <dd>

<span data-ttu-id="94725-112">As definições de tempo fundamentais de uma função de animação; Eles são os primitivos dos quais funções de animação mais complexas e de nível mais alto são criadas.</span><span class="sxs-lookup"><span data-stu-id="94725-112">The fundamental timing definitions of an animation function; they are the primitives from which more complex and higher level animation functions are built.</span></span>

</dd> <dt>

<span data-ttu-id="94725-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**buffer de fundo**</span><span class="sxs-lookup"><span data-stu-id="94725-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**back buffer**</span></span>
</dt> <dd>

<span data-ttu-id="94725-114">Um retângulo de memória no qual um aplicativo pode gravar diretamente.</span><span class="sxs-lookup"><span data-stu-id="94725-114">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="94725-115">O buffer de fundo nunca é exibido diretamente no monitor.</span><span class="sxs-lookup"><span data-stu-id="94725-115">The back buffer is never directly displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="94725-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**lote**</span><span class="sxs-lookup"><span data-stu-id="94725-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**</span></span>
</dt> <dd>

<span data-ttu-id="94725-117">Um grupo de chamadas de método DirectComposition processadas atomicamente.</span><span class="sxs-lookup"><span data-stu-id="94725-117">A group of DirectComposition method calls that are processed atomically.</span></span>

</dd> <dt>

<span data-ttu-id="94725-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span><span class="sxs-lookup"><span data-stu-id="94725-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="94725-119">Um buffer de cores, com ou sem um canal alfa, que reside no sistema ou na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="94725-119">A color buffer, either with or without an alpha channel, that resides in system or video memory.</span></span>

</dd> <dt>

<span data-ttu-id="94725-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**modo de borda**</span><span class="sxs-lookup"><span data-stu-id="94725-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**border mode**</span></span>
</dt> <dd>

<span data-ttu-id="94725-121">Uma propriedade de um Visual DirectComposition da Microsoft que afeta como as bordas de um bitmap são compostas quando o bitmap é transformado de modo que as bordas não são alinhadas por eixo com coordenadas de inteiros.</span><span class="sxs-lookup"><span data-stu-id="94725-121">A property of a Microsoft DirectComposition visual that affects how the edges of a bitmap are composed when the bitmap is transformed such that the edges are not axis-aligned with integer coordinates.</span></span> <span data-ttu-id="94725-122">Ele também afeta como o conteúdo é recortado nos cantos de um clipe que tem cantos arredondados e na borda de um clipe que é transformado de modo que as bordas não são alinhadas ao eixo com coordenadas de inteiros.</span><span class="sxs-lookup"><span data-stu-id="94725-122">It also affects how content is clipped at the corners of a clip that has rounded corners, and at the edge of a clip that is transformed such that the edges are not axis-aligned with integer coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="94725-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**objeto de clipe**</span><span class="sxs-lookup"><span data-stu-id="94725-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip object**</span></span>
</dt> <dd>

<span data-ttu-id="94725-124">Um objeto que representa um retângulo de clipe.</span><span class="sxs-lookup"><span data-stu-id="94725-124">A object that represents a clip rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="94725-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**retângulo do clipe**</span><span class="sxs-lookup"><span data-stu-id="94725-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**clip rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="94725-126">Um conjunto de coordenadas que definem a área do conteúdo de bitmap do Visual que é desenhada na tela quando o bitmap é renderizado.</span><span class="sxs-lookup"><span data-stu-id="94725-126">A set of coordinates that define the area of visual's bitmap content that is drawn on the screen when the bitmap is rendered.</span></span>

</dd> <dt>

<span data-ttu-id="94725-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**coberta**</span><span class="sxs-lookup"><span data-stu-id="94725-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**cloak**</span></span>
</dt> <dd>

<span data-ttu-id="94725-128">Para impedir temporariamente Gerenciador de Janelas da Área de Trabalho (DWM) de desenhar uma janela para a exibição.</span><span class="sxs-lookup"><span data-stu-id="94725-128">To temporarily prevent Desktop Window Manager (DWM) from drawing a window to the display.</span></span> <span data-ttu-id="94725-129">Normalmente, os aplicativos encobrir uma janela enquanto o DirectComposition usa o bitmap da janela em uma composição.</span><span class="sxs-lookup"><span data-stu-id="94725-129">Applications typically cloak a window while DirectComposition uses the window's bitmap in a composition.</span></span>

</dd> <dt>

<span data-ttu-id="94725-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**compromisso**</span><span class="sxs-lookup"><span data-stu-id="94725-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="94725-131">Para enviar um lote de comandos para o DirectCompositionDirectComposition para processamento.</span><span class="sxs-lookup"><span data-stu-id="94725-131">To submit a batch of commands to DirectCompositionDirectComposition for processing.</span></span>

</dd> <dt>

<span data-ttu-id="94725-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**modo composto**</span><span class="sxs-lookup"><span data-stu-id="94725-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**composite mode**</span></span>
</dt> <dd>

<span data-ttu-id="94725-133">Uma das várias maneiras de mesclar dois bitmaps (uma origem e um destino) para atingir um efeito específico.</span><span class="sxs-lookup"><span data-stu-id="94725-133">One of several ways of blending two bitmaps (a source and a destination) to achieve a particular effect.</span></span>

</dd> <dt>

<span data-ttu-id="94725-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composição**</span><span class="sxs-lookup"><span data-stu-id="94725-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**</span></span>
</dt> <dd>

<span data-ttu-id="94725-135">Uma coleção de bitmaps que são combinados e manipulados aplicando-se várias transformações, efeitos e animações para produzir um resultado Visual pretendido em uma interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94725-135">A collection of bitmaps that are combined and manipulated by applying various transforms, effects, and animations to produce an intended visual result in an application UI.</span></span>

</dd> <dt>

<span data-ttu-id="94725-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**janela de destino da composição**</span><span class="sxs-lookup"><span data-stu-id="94725-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**composition target window**</span></span>
</dt> <dd>

<span data-ttu-id="94725-137">A janela à qual uma árvore visual está associada e na qual a composição resultante é desenhada.</span><span class="sxs-lookup"><span data-stu-id="94725-137">The window to which a visual tree is bound, and in which the resulting composition is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="94725-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**funciona**</span><span class="sxs-lookup"><span data-stu-id="94725-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effect**</span></span>
</dt> <dd>

<span data-ttu-id="94725-139">Uma operação que modifica como os bitmaps de uma árvore visual são rasterizados, normalmente aplicando um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="94725-139">An operation that modifies how the bitmaps of a visual tree are rasterized, typically by applying a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="94725-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**grupo de efeitos**</span><span class="sxs-lookup"><span data-stu-id="94725-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**effect group**</span></span>
</dt> <dd>

<span data-ttu-id="94725-141">Um grupo de efeitos de bitmap que são aplicados em conjunto para modificar a rasterização da subárvore de um Visual.</span><span class="sxs-lookup"><span data-stu-id="94725-141">A group of bitmap effects that are applied together to modify the rasterization of a visual’s sub-tree.</span></span>

</dd> <dt>

<span data-ttu-id="94725-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**quadro**</span><span class="sxs-lookup"><span data-stu-id="94725-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="94725-143">Uma iteração do mecanismo de composição que produz uma rasterização da árvore visual.</span><span class="sxs-lookup"><span data-stu-id="94725-143">An iteration of the composition engine that produces a rasterization of the visual tree.</span></span>

</dd> <dt>

<span data-ttu-id="94725-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**buffer frontal**</span><span class="sxs-lookup"><span data-stu-id="94725-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**front buffer**</span></span>
</dt> <dd>

<span data-ttu-id="94725-145">Um retângulo de memória que é convertido pelo adaptador gráfico e exibido no monitor.</span><span class="sxs-lookup"><span data-stu-id="94725-145">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="94725-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**modo de interpolação**</span><span class="sxs-lookup"><span data-stu-id="94725-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**interpolation mode**</span></span>
</dt> <dd>

<span data-ttu-id="94725-147">Uma propriedade que determina como um bitmap é composto quando é transformado, de modo que não há uma correspondência de um para um entre pixels no bitmap e em pixels na tela.</span><span class="sxs-lookup"><span data-stu-id="94725-147">A property that determines how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.</span></span>

</dd> <dt>

<span data-ttu-id="94725-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**Visual raiz**</span><span class="sxs-lookup"><span data-stu-id="94725-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**root visual**</span></span>
</dt> <dd>

<span data-ttu-id="94725-149">O Visual do qual todos os outros visuais em uma árvore visual são descendentes.</span><span class="sxs-lookup"><span data-stu-id="94725-149">The visual from which all other visuals in a visual tree are descended.</span></span>

</dd> <dt>

<span data-ttu-id="94725-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**Cadeia de permuta**</span><span class="sxs-lookup"><span data-stu-id="94725-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="94725-151">Uma coleção de um ou mais buffers de fundo que podem ser exibidos em série para o buffer frontal</span><span class="sxs-lookup"><span data-stu-id="94725-151">A collection of one or more back buffers that can be serially presented to the front buffer</span></span>

</dd> <dt>

<span data-ttu-id="94725-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**tona**</span><span class="sxs-lookup"><span data-stu-id="94725-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surface**</span></span>
</dt> <dd>

<span data-ttu-id="94725-153">Uma representação de uma área linear da memória de exibição que geralmente reside na memória de vídeo do cartão de vídeo, embora as superfícies possam existir na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="94725-153">A representation of a linear area of display memory that usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="94725-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**tenha**</span><span class="sxs-lookup"><span data-stu-id="94725-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="94725-155">Uma matriz que representa uma transformação de coordenadas em um espaço bidimensional ou tridimensional.</span><span class="sxs-lookup"><span data-stu-id="94725-155">A matrix that represents a coordinate transformation in either two-dimensional or three-dimensional space.</span></span>

</dd> <dt>

<span data-ttu-id="94725-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**grupo de transformação**</span><span class="sxs-lookup"><span data-stu-id="94725-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transform group**</span></span>
</dt> <dd>

<span data-ttu-id="94725-157">Uma coleção de transformações cujas matrizes são multiplicadas em conjunto na ordem em que são especificadas na coleção antes de serem aplicadas a um Visual.</span><span class="sxs-lookup"><span data-stu-id="94725-157">A collection of transforms whose matrices are multiplied together in the order in which they are specified in the collection before they are applied to a visual.</span></span>

</dd> <dt>

<span data-ttu-id="94725-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visualizar**</span><span class="sxs-lookup"><span data-stu-id="94725-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**visual**</span></span>
</dt> <dd>

<span data-ttu-id="94725-159">Um objeto que contém uma referência opcional a um objeto de bitmap e um conjunto de propriedades que determinam onde e como o bitmap é renderizado na tela.</span><span class="sxs-lookup"><span data-stu-id="94725-159">An object that contains an optional reference to a bitmap object, and a set of properties that determine where and how the bitmap is rendered to the screen.</span></span>

</dd> <dt>

<span data-ttu-id="94725-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**objeto visual**</span><span class="sxs-lookup"><span data-stu-id="94725-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visual object**</span></span>
</dt> <dd>

<span data-ttu-id="94725-161">Consulte [*Visual*](/windows).</span><span class="sxs-lookup"><span data-stu-id="94725-161">See [*visual*](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="94725-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**subárvore Visual**</span><span class="sxs-lookup"><span data-stu-id="94725-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visual subtree**</span></span>
</dt> <dd>

<span data-ttu-id="94725-163">Uma parte de uma árvore visual que consiste em um Visual específico e todos os seus visuais filho e descendentes.</span><span class="sxs-lookup"><span data-stu-id="94725-163">A portion of a visual tree consisting of a particular visual and all of its child and descendent visuals.</span></span>

</dd> <dt>

<span data-ttu-id="94725-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**árvore visual**</span><span class="sxs-lookup"><span data-stu-id="94725-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visual tree**</span></span>
</dt> <dd>

<span data-ttu-id="94725-165">Uma coleção hierárquica de visuais usados para criar uma composição.</span><span class="sxs-lookup"><span data-stu-id="94725-165">A hierarchical collection of visuals used to create a composition.</span></span>

</dd> <dt>

<span data-ttu-id="94725-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**Cadeia de permuta sem janela**</span><span class="sxs-lookup"><span data-stu-id="94725-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**windowless swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="94725-167">Uma cadeia de permuta associada a um objeto visual DirectComposition em vez de uma janela.</span><span class="sxs-lookup"><span data-stu-id="94725-167">A swap chain that is associated with a DirectComposition visual object instead of a window.</span></span>

</dd> </dl>

 

 