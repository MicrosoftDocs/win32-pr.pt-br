---
title: Elemento TEXT (SDK do Windows Media Player)
description: Elemento de texto
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Capas do Windows Media Player, elemento de texto
- capas, elemento TEXT
- Elemento de texto
- referência de capas, elemento de texto
- elementos, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acdad737fda44cc0e090eb13fb20c765b447ccbd
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104293546"
---
# <a name="text-element"></a>Elemento de texto

O elemento **Text** fornece uma maneira de criar e controlar a aparência do texto dentro de uma capa usando os atributos a seguir. Elementos de **texto** predefinidos também são fornecidos para sua conveniência.

O elemento **Text** dá suporte aos seguintes atributos.



| Atributo                                                   | Descrição                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](text-backgroundcolor.md)                 | Especifica ou recupera a cor do plano de fundo do controle de texto.                                           |
| [cursor](text-cursor.md)                                   | Especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle de texto.     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | Especifica ou recupera a cor do plano de fundo usada para o controle de texto quando ele está desabilitado.                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | Especifica ou recupera o estilo de fonte usado para o controle de texto quando ele está desabilitado.                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | Especifica ou recupera a cor do texto usada quando o controle de texto está desabilitado.                               |
| [fontFace](text-fontface.md)                               | Especifica ou recupera o tipo de fonte para o controle de texto.                                                   |
| [fontSize](text-fontsize.md)                               | Especifica ou recupera o tamanho da fonte para o controle de texto.                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | Especifica ou recupera um valor que indica se a suavização de fontes está habilitada.                                |
| [fontStyle](text-fontstyle.md)                             | Especifica ou recupera o estilo da fonte para o controle de texto.                                                 |
| [foregroundColor](text-foregroundcolor.md)                 | Especifica ou recupera a cor do texto para o controle de texto.                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | Especifica ou recupera a cor de plano de fundo usada para o controle de texto quando o cursor do mouse passa sobre ele. |
| [hoverFontStyle](text-hoverfontstyle.md)                   | Especifica ou recupera o estilo de fonte usado para o controle de texto quando o cursor do mouse passa sobre ele.       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | Especifica ou recupera a cor de texto usada para o controle de texto quando o cursor do mouse passa sobre ele.       |
| [elabora](text-justification.md)                     | Especifica ou recupera o alinhamento do texto dentro do controle de texto.                                   |
| [rolagem](text-scrolling.md)                             | Especifica ou recupera um valor que indica se o texto rola.                                         |
| [scrollingAmount](text-scrollingamount.md)                 | Especifica ou recupera o número de pixels que o texto move durante cada movimento de rolagem.             |
| [scrollingDelay](text-scrollingdelay.md)                   | Especifica ou recupera o intervalo de tempo entre movimentos de rolagem.                                          |
| [scrollingDirection](text-scrollingdirection.md)           | Especifica ou recupera a direção do texto de rolagem.                                                 |
| [TextWidth](text-textwidth.md)                             | Recupera a largura em pixels da cadeia de caracteres contida no atributo de **valor** .                           |
| [Dessa](text-tooltip.md)                                 | Especifica ou recupera o texto da dica de ferramenta para o controle de texto.                                               |
| [value](text-value.md)                                     | Especifica ou recupera o texto que é exibido no controle de texto.                                      |
| [Quebra](text-wordwrap.md)                               | Especifica ou recupera um valor que indica se a quebra automática de texto está habilitada ou desabilitada.                     |



 

O elemento **Text** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente. Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md).

Elementos de texto predefinidos são elementos de **texto** normais com várias configurações de atributo comuns especificadas por padrão. Os seguintes elementos de texto predefinidos estão disponíveis.



| TEXTO predefinido                                | Descrição                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | Um elemento de **texto** com um ouvinte interno para **Player. Controls. currentPositionString**. |
| [DURATIONTEXT](durationtext.md)               | Um elemento de **texto** com um ouvinte interno para **Player. currentMedia. durationstring**.    |
| [STATUSTEXT](statustext.md)                   | Um elemento de **texto** com um ouvinte interno para **Player. status**.                         |
| [TRACKNAMETEXT](tracknametext.md)             | Um elemento de **texto** com um ouvinte interno para **Player.currentMedia.Name**.              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




