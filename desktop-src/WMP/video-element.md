---
title: Elemento VIDEO
description: Elemento VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player capas, elemento VIDEO
- capas, elemento VIDEO
- Elemento VIDEO
- referência para capas, elemento VIDEO
- elementos, vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b72df7472829fe9979c9f7a30558e340a69aeb2f7024641623ba6be1a46424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054194"
---
# <a name="video-element"></a>Elemento VIDEO

O elemento **Video** fornece uma maneira de manipular uma janela de vídeo em uma capa, usando os seguintes atributos e eventos. Um elemento de **vídeo** predefinido também é fornecido para sua conveniência.

O elemento **Video** dá suporte aos seguintes atributos.



| Atributo                                            | Descrição                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](video-backgroundcolor.md)         | Especifica ou recupera a cor do plano de fundo do controle de vídeo.                                                                                                                                                                        |
| [cursor](video-cursor.md)                           | Especifica ou recupera o valor do cursor que é usado quando o mouse está sobre uma área clicável do vídeo.                                                                                                                               |
| [Tela inteira](video-fullscreen.md)                   | Especifica ou recupera um valor que indica se o vídeo é exibido no modo de tela inteira. Só pode ser definido em tempo de execução.                                                                                                               |
| [maintainAspectRatio](video-maintainaspectratio.md) | Especifica ou recupera um valor que indica se o vídeo manterá a taxa de proporção ao tentar se ajustar dentro da largura e altura definidas para o controle.                                                                       |
| [shrinkToFit](video-shrinktofit.md)                 | Especifica ou recupera um valor que indica se o vídeo será reduzido para a largura e a altura definidas para o controle de vídeo.                                                                                                           |
| [stretchToFit](video-stretchtofit.md)               | Especifica ou recupera um valor que indica se o vídeo se alongará para a largura e a altura definidas para o controle de vídeo.                                                                                                   |
| [toolTip](video-tooltip.md)                         | Especifica ou recupera o texto da dica de ferramenta para a janela de vídeo.                                                                                                                                                                            |
| [sem janela](video-windowless.md)                   | Especifica ou recupera um valor que indica se o controle de vídeo será com janela ou sem janela; ou seja, se todo o retângulo do controle estará visível sempre ou puder ser recortado. Só pode ser definido em tempo de design. |
| [aplicar](video-zoom.md)                               | Especifica a porcentagem de escala do vídeo.                                                                                                                                                                                    |



 

O elemento **Video** pode implementar os manipuladores de eventos a seguir.



| Manipulador de eventos                          | Descrição                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | Manipula um evento que ocorre quando o vídeo para de renderizar e é descarregado. |
| [onvideostart](video-onvideostart.md) | Manipula um evento que ocorre quando o vídeo é carregado e começa a ser renderizado.  |



 

O elemento **Video** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente, exceto quando indicado. Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md).

Elementos de vídeo predefinidos são elementos de **vídeo** normais com várias configurações de atributo comuns especificadas por padrão. Os seguintes elementos de vídeo predefinidos estão disponíveis.



| VÍDEO predefinido         | Descrição                                                |
|--------------------------|------------------------------------------------------------|
| [WMPVIDEO](wmpvideo.md) | Um elemento de **vídeo** que amplia o vídeo quando redimensionado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




