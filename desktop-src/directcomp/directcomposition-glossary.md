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
# <a name="directcomposition-glossary"></a>Glossário do DirectComposition

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico define os termos do Microsoft DirectComposition.

<dl> <dt>

<span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**função de animação**
</dt> <dd>

Uma construção que especifica como o valor de uma única propriedade de objeto é alterado ao longo de um período de tempo.

</dd> <dt>

<span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**objeto de animação**
</dt> <dd>

Um objeto que representa uma função para animar as propriedades de outro objeto.

</dd> <dt>

<span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segmento de animação**
</dt> <dd>

As definições de tempo fundamentais de uma função de animação; Eles são os primitivos dos quais funções de animação mais complexas e de nível mais alto são criadas.

</dd> <dt>

<span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**buffer de fundo**
</dt> <dd>

Um retângulo de memória no qual um aplicativo pode gravar diretamente. O buffer de fundo nunca é exibido diretamente no monitor.

</dd> <dt>

<span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**lote**
</dt> <dd>

Um grupo de chamadas de método DirectComposition processadas atomicamente.

</dd> <dt>

<span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**
</dt> <dd>

Um buffer de cores, com ou sem um canal alfa, que reside no sistema ou na memória de vídeo.

</dd> <dt>

<span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**modo de borda**
</dt> <dd>

Uma propriedade de um Visual DirectComposition da Microsoft que afeta como as bordas de um bitmap são compostas quando o bitmap é transformado de modo que as bordas não são alinhadas por eixo com coordenadas de inteiros. Ele também afeta como o conteúdo é recortado nos cantos de um clipe que tem cantos arredondados e na borda de um clipe que é transformado de modo que as bordas não são alinhadas ao eixo com coordenadas de inteiros.

</dd> <dt>

<span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**objeto de clipe**
</dt> <dd>

Um objeto que representa um retângulo de clipe.

</dd> <dt>

<span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**retângulo do clipe**
</dt> <dd>

Um conjunto de coordenadas que definem a área do conteúdo de bitmap do Visual que é desenhada na tela quando o bitmap é renderizado.

</dd> <dt>

<span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**coberta**
</dt> <dd>

Para impedir temporariamente Gerenciador de Janelas da Área de Trabalho (DWM) de desenhar uma janela para a exibição. Normalmente, os aplicativos encobrir uma janela enquanto o DirectComposition usa o bitmap da janela em uma composição.

</dd> <dt>

<span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**compromisso**
</dt> <dd>

Para enviar um lote de comandos para o DirectCompositionDirectComposition para processamento.

</dd> <dt>

<span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**modo composto**
</dt> <dd>

Uma das várias maneiras de mesclar dois bitmaps (uma origem e um destino) para atingir um efeito específico.

</dd> <dt>

<span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composição**
</dt> <dd>

Uma coleção de bitmaps que são combinados e manipulados aplicando-se várias transformações, efeitos e animações para produzir um resultado Visual pretendido em uma interface do usuário do aplicativo.

</dd> <dt>

<span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**janela de destino da composição**
</dt> <dd>

A janela à qual uma árvore visual está associada e na qual a composição resultante é desenhada.

</dd> <dt>

<span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**funciona**
</dt> <dd>

Uma operação que modifica como os bitmaps de uma árvore visual são rasterizados, normalmente aplicando um sombreador de pixel.

</dd> <dt>

<span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**grupo de efeitos**
</dt> <dd>

Um grupo de efeitos de bitmap que são aplicados em conjunto para modificar a rasterização da subárvore de um Visual.

</dd> <dt>

<span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**quadro**
</dt> <dd>

Uma iteração do mecanismo de composição que produz uma rasterização da árvore visual.

</dd> <dt>

<span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**buffer frontal**
</dt> <dd>

Um retângulo de memória que é convertido pelo adaptador gráfico e exibido no monitor.

</dd> <dt>

<span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**modo de interpolação**
</dt> <dd>

Uma propriedade que determina como um bitmap é composto quando é transformado, de modo que não há uma correspondência de um para um entre pixels no bitmap e em pixels na tela.

</dd> <dt>

<span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**Visual raiz**
</dt> <dd>

O Visual do qual todos os outros visuais em uma árvore visual são descendentes.

</dd> <dt>

<span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**Cadeia de permuta**
</dt> <dd>

Uma coleção de um ou mais buffers de fundo que podem ser exibidos em série para o buffer frontal

</dd> <dt>

<span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**tona**
</dt> <dd>

Uma representação de uma área linear da memória de exibição que geralmente reside na memória de vídeo do cartão de vídeo, embora as superfícies possam existir na memória do sistema.

</dd> <dt>

<span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**tenha**
</dt> <dd>

Uma matriz que representa uma transformação de coordenadas em um espaço bidimensional ou tridimensional.

</dd> <dt>

<span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**grupo de transformação**
</dt> <dd>

Uma coleção de transformações cujas matrizes são multiplicadas em conjunto na ordem em que são especificadas na coleção antes de serem aplicadas a um Visual.

</dd> <dt>

<span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visualizar**
</dt> <dd>

Um objeto que contém uma referência opcional a um objeto de bitmap e um conjunto de propriedades que determinam onde e como o bitmap é renderizado na tela.

</dd> <dt>

<span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**objeto visual**
</dt> <dd>

Consulte [*Visual*](/windows).

</dd> <dt>

<span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**subárvore Visual**
</dt> <dd>

Uma parte de uma árvore visual que consiste em um Visual específico e todos os seus visuais filho e descendentes.

</dd> <dt>

<span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**árvore visual**
</dt> <dd>

Uma coleção hierárquica de visuais usados para criar uma composição.

</dd> <dt>

<span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**Cadeia de permuta sem janela**
</dt> <dd>

Uma cadeia de permuta associada a um objeto visual DirectComposition em vez de uma janela.

</dd> </dl>

 

 