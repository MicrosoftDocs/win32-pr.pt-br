---
title: Elemento SLIDER
description: Elemento SLIDER
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Windows Media Player capas, elemento SLIDER
- skins, elemento SLIDER
- Elemento SLIDER
- referência para capas, elemento SLIDER
- elementos, SLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140c84f6bec826b34ff4e1c5a4a3365d44ba9aa67ca9504cea642aba25f076d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569079"
---
# <a name="slider-element"></a>Elemento SLIDER

O **elemento SLIDER** fornece uma maneira de criar e manipular um controle deslizante horizontal ou vertical simples. Ele dá suporte aos seguintes atributos e manipuladores de eventos. Elementos **SLIDER predefinidos** também são fornecidos para conveniência.

O **elemento SLIDER** dá suporte aos atributos a seguir.



| Atributo                                                 | Descrição                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](slider-backgroundcolor.md)             | Especifica ou recupera a cor da tela de fundo do controle deslizante.                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | Especifica ou recupera a cor final da tela de fundo do controle deslizante.                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | Especifica ou recupera a imagem de plano de fundo do controle deslizante que aparece ao passar o mouse sobre ela.      |
| [backgroundImage](slider-backgroundimage.md)             | Especifica ou recupera a imagem de plano de fundo padrão do controle deslizante.                                                |
| [Bordersize](slider-bordersize.md)                       | Especifica ou recupera o tamanho da borda em pixels.                                                                 |
| [cursor](slider-cursor.md)                               | Especifica ou recupera um valor que indica qual tipo de cursor aparece quando o mouse está sobre o controle deslizante. |
| [direction](slider-direction.md)                         | Especifica ou recupera a direção em que as imagens do controle deslizante são colocadas.                                             |
| [disabledColor](slider-disabledcolor.md)                 | Especifica ou recupera a cor desabilitada do controle deslizante.                                                  |
| [disabledImage](slider-disabledimage.md)                 | Especifica ou recupera a imagem do controle deslizante que aparece quando o controle está desabilitado.                         |
| [Foregroundcolor](slider-foregroundcolor.md)             | Especifica ou recupera a cor de primeiro plano do controle deslizante.                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | Especifica ou recupera a cor final de primeiro plano do controle deslizante.                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | Especifica ou recupera a imagem de primeiro plano do controle deslizante que aparece ao passar o mouse sobre ela.      |
| [foregroundImage](slider-foregroundimage.md)             | Especifica ou recupera a imagem de primeiro plano padrão do controle deslizante.                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | Especifica ou recupera a posição atual da barra de progresso em primeiro plano como uma porcentagem da área do controle deslizante.    |
| [max](slider-max.md)                                     | Especifica ou recupera o valor máximo do intervalo definido pelo controle deslizante.                              |
| [min](slider-min.md)                                     | Especifica ou recupera o valor mínimo do intervalo definido pelo controle deslizante.                              |
| [Slide](slider-slide.md)                                 | Especifica ou recupera um valor que indica se a imagem de primeiro plano desliza sobre a imagem de plano de fundo.          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | Especifica ou recupera a imagem de miniatura desabilitada do controle deslizante.                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | Especifica ou recupera a imagem que representa o estado para baixo do polegar.                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | Especifica ou recupera a imagem do polegar que aparece ao passar o mouse sobre ela.                  |
| [thumbImage](slider-thumbimage.md)                       | Especifica ou recupera a imagem que será usada para representar a posição atual do controle deslizante.               |
| [Azulejos](slider-tiled.md)                                 | Especifica ou recupera um valor que indica se as imagens do controle deslizante serão lado a lado.                                |
| [toolTip](slider-tooltip.md)                             | Especifica ou recupera o texto da Dica de Ferramenta para o controle deslizante.                                                   |
| [transparencyColor](slider-transparencycolor.md)         | Especifica ou recupera a cor transparente das imagens do controle deslizante.                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | Especifica ou recupera um valor que indica se a barra de progresso em primeiro plano será usada.                       |
| [value](slider-value.md)                                 | Especifica e recupera a posição atual do controle deslizante.                                                       |



 

O **elemento SLIDER** pode implementar os manipuladores de eventos a seguir.



| Manipulador de eventos                                   | Descrição                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | Trata um evento que ocorre quando o usuário clica e mantém o botão esquerdo do mouse para baixo e começa a arrastar o mouse. |
| [onDragEnd](slider-ondragend.md)               | Trata um evento que ocorre quando o botão esquerdo do mouse é liberado após uma operação de arrastar.                      |
| [onPositionChange](slider-onpositionchange.md) | Trata um evento que ocorre quando a posição do controle deslizante muda como resultado do usuário clicar ou arrastar.   |



 

O **elemento SLIDER** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente. Para obter mais informações, consulte [Atributos de ambiente e](ambient-attributes.md) [manipuladores de eventos de ambiente](ambient-event-handlers.md).

Os controles deslizantes predefinidos são elementos **SLIDER normais** com várias configurações de atributo comuns especificadas por padrão. Os controles deslizantes predefinidos a seguir estão disponíveis.



| SLIDER predefinido                  | Descrição                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | Um **CONTROLE DESLIZANTE** usado para definir o balanceador de áudio.                        |
| [SEEKSLIDER](seekslider.md)       | Um **CONTROLE DESLIZANTE** usado para buscar qualquer posição dentro de um arquivo de mídia. |
| [VOLUMESLIDER](volumeslider.md)   | Um **CONTROLE DESLIZANTE** usado para definir o volume de áudio.                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




