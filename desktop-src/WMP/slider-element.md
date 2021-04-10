---
title: Elemento SLIDER
description: Elemento SLIDER
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Capas do Windows Media Player, elemento SLIDER
- capas, elemento SLIDER
- Elemento SLIDER
- referência para capas, elemento SLIDER
- elementos, controle deslizante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34607c8706fccc8f416ebc83ae483c98a784c08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292324"
---
# <a name="slider-element"></a>Elemento SLIDER

O elemento **Slider** fornece uma maneira de criar e manipular um controle deslizante horizontal simples ou vertical. Ele dá suporte aos seguintes atributos e manipuladores de eventos. Elementos **Slider** predefinidos também são fornecidos para sua conveniência.

O elemento **Slider** dá suporte aos seguintes atributos.



| Atributo                                                 | Descrição                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](slider-backgroundcolor.md)             | Especifica ou recupera a cor do plano de fundo do controle deslizante.                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | Especifica ou recupera a cor final do plano de fundo do controle deslizante.                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | Especifica ou recupera a imagem de plano de fundo do controle deslizante que aparece ao passar o mouse sobre ele.      |
| [backgroundImage](slider-backgroundimage.md)             | Especifica ou recupera a imagem de plano de fundo padrão do controle deslizante.                                                |
| [Bordas](slider-bordersize.md)                       | Especifica ou recupera o tamanho da borda em pixels.                                                                 |
| [cursor](slider-cursor.md)                               | Especifica ou recupera um valor que indica qual tipo de cursor aparece quando o mouse está sobre o controle deslizante. |
| [direction](slider-direction.md)                         | Especifica ou recupera a direção na qual as imagens do controle deslizante são dispostas.                                             |
| [disabledColor](slider-disabledcolor.md)                 | Especifica ou recupera a cor desabilitada do controle deslizante.                                                  |
| [disabledImage](slider-disabledimage.md)                 | Especifica ou recupera a imagem do controle deslizante que aparece quando o controle está desabilitado.                         |
| [foregroundColor](slider-foregroundcolor.md)             | Especifica ou recupera a cor de primeiro plano do controle deslizante.                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | Especifica ou recupera a cor final do primeiro plano do controle deslizante.                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | Especifica ou recupera a imagem em primeiro plano do controle deslizante que aparece ao passar o mouse sobre ele.      |
| [foregroundImage](slider-foregroundimage.md)             | Especifica ou recupera a imagem de primeiro plano padrão do controle deslizante.                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | Especifica ou recupera a posição atual da barra de progresso em primeiro plano como uma porcentagem da área do controle deslizante.    |
| [max](slider-max.md)                                     | Especifica ou recupera o valor máximo do intervalo definido pelo controle deslizante.                              |
| [min](slider-min.md)                                     | Especifica ou recupera o valor mínimo do intervalo definido pelo controle deslizante.                              |
| [seleto](slider-slide.md)                                 | Especifica ou recupera um valor que indica se a imagem em primeiro plano desliza sobre a imagem de plano de fundo.          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | Especifica ou recupera a imagem Thumb desabilitada do controle deslizante.                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | Especifica ou recupera a imagem que representa o estado inoperante do Thumb.                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | Especifica ou recupera a imagem do Thumb que aparece ao passar o mouse sobre ela.                  |
| [thumbImage](slider-thumbimage.md)                       | Especifica ou recupera a imagem que será usada para representar a posição atual do controle deslizante.               |
| [lado a lado](slider-tiled.md)                                 | Especifica ou recupera um valor que indica se as imagens do controle deslizante serão enlados.                                |
| [Dessa](slider-tooltip.md)                             | Especifica ou recupera o texto da dica de ferramenta para o controle deslizante.                                                   |
| [transparencyColor](slider-transparencycolor.md)         | Especifica ou recupera a cor transparente das imagens do controle deslizante.                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | Especifica ou recupera um valor que indica se a barra de progresso de primeiro plano será usada.                       |
| [value](slider-value.md)                                 | Especifica e recupera a posição atual do controle deslizante.                                                       |



 

O elemento **Slider** pode implementar os manipuladores de eventos a seguir.



| Manipulador de eventos                                   | Descrição                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | Manipula um evento que ocorre quando o usuário clica e mantém o botão esquerdo do mouse pressionado e começa a arrastar o mouse. |
| [onDragEnd](slider-ondragend.md)               | Manipula um evento que ocorre quando o botão esquerdo do mouse é liberado após uma operação de arrastar.                      |
| [onPositionChange](slider-onpositionchange.md) | Manipula um evento que ocorre quando a posição do controle deslizante é alterada como resultado do clique ou arraste do usuário.   |



 

O elemento **Slider** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente. Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md).

Os controles deslizantes predefinidos são elementos **Slider** normais com várias configurações de atributo comuns especificadas por padrão. Os seguintes controles deslizantes predefinidos estão disponíveis.



| Controle deslizante predefinido                  | Descrição                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | Um **controle deslizante** usado para definir o equilíbrio de áudio.                        |
| [SEEKSLIDER](seekslider.md)       | Um **controle deslizante** usado para buscar qualquer posição dentro de um arquivo de mídia. |
| [VOLUMESLIDER](volumeslider.md)   | Um **controle deslizante** usado para definir o volume de áudio.                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




