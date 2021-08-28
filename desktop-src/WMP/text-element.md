---
title: Elemento TEXT (Windows Media Player SDK)
description: Elemento TEXT
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Windows Media Player capas, elemento TEXT
- skins, elemento TEXT
- Elemento TEXT
- referência para capas, elemento TEXT
- elements,TEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c0d30393ef4fdeb62061ee58b0c7bd2f3f58bd685945e62c0e8062f22d881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122846"
---
# <a name="text-element"></a>Elemento TEXT

O **elemento TEXT** fornece uma maneira de criar e controlar a aparência do texto em uma capa usando os atributos a seguir. Elementos TEXT **predefinidos** também são fornecidos para conveniência.

O **elemento TEXT** dá suporte aos atributos a seguir.



| Atributo                                                   | Descrição                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](text-backgroundcolor.md)                 | Especifica ou recupera a cor da tela de fundo do controle Texto.                                           |
| [cursor](text-cursor.md)                                   | Especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle Texto.     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | Especifica ou recupera a cor da tela de fundo usada para o controle Texto quando ele está desabilitado.                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | Especifica ou recupera o estilo de fonte usado para o controle Texto quando ele é desabilitado.                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | Especifica ou recupera a cor do texto usada quando o controle Texto está desabilitado.                               |
| [fontFace](text-fontface.md)                               | Especifica ou recupera a face de tipo para o controle Texto.                                                   |
| [Fontsize](text-fontsize.md)                               | Especifica ou recupera o tamanho da fonte para o controle Texto.                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | Especifica ou recupera um valor que indica se a suavização de fonte está habilitada.                                |
| [Fontstyle](text-fontstyle.md)                             | Especifica ou recupera o estilo da fonte para o controle Texto.                                                 |
| [Foregroundcolor](text-foregroundcolor.md)                 | Especifica ou recupera a cor do texto para o controle Texto.                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | Especifica ou recupera a cor da tela de fundo usada para o controle Texto quando o cursor do mouse sobre ele. |
| [hoverFontStyle](text-hoverfontstyle.md)                   | Especifica ou recupera o estilo de fonte usado para o controle Texto quando o cursor do mouse sobre ele.       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | Especifica ou recupera a cor do texto usada para o controle Texto quando o cursor do mouse sobre ele.       |
| [Justificação](text-justification.md)                     | Especifica ou recupera o alinhamento do texto dentro do controle Texto.                                   |
| [Rolagem](text-scrolling.md)                             | Especifica ou recupera um valor que indica se o texto rola.                                         |
| [scrollingAmount](text-scrollingamount.md)                 | Especifica ou recupera o número de pixels que o texto move durante cada movimento de rolagem.             |
| [scrollingDelay](text-scrollingdelay.md)                   | Especifica ou recupera o atraso de tempo entre os movimentos de rolagem.                                          |
| [scrollingDirection](text-scrollingdirection.md)           | Especifica ou recupera a direção do texto de rolagem.                                                 |
| [Textwidth](text-textwidth.md)                             | Recupera a largura em pixels da cadeia de caracteres contida no atributo **value.**                           |
| [toolTip](text-tooltip.md)                                 | Especifica ou recupera o texto da Dica de Ferramenta para o controle de texto.                                               |
| [value](text-value.md)                                     | Especifica ou recupera o texto exibido no controle Texto.                                      |
| [Wordwrap](text-wordwrap.md)                               | Especifica ou recupera um valor que indica se o quebra-texto está habilitado ou desabilitado.                     |



 

O **elemento TEXT** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente. Para obter mais informações, consulte [Atributos de ambiente e](ambient-attributes.md) [manipuladores de eventos de ambiente](ambient-event-handlers.md).

Elementos de texto predefinidos são **elementos TEXT normais** com várias configurações de atributo comuns especificadas por padrão. Os seguintes elementos de texto predefinidos estão disponíveis.



| TEXTO predefinido                                | Descrição                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | Um **elemento TEXT** com um ouvinte integrado para **player.controls.currentPositionString**. |
| [DURATIONTEXT](durationtext.md)               | Um **elemento TEXT** com um ouvinte integrado para **player.currentMedia.DurationString.**    |
| [Statustext](statustext.md)                   | Um **elemento TEXT** com um ouvinte integrado para **player.status**.                         |
| [TRACKNAMETEXT](tracknametext.md)             | Um **elemento TEXT** com um ouvinte integrado para **player.currentMedia.name**.              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




