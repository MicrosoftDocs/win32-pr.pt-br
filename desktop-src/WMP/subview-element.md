---
title: Elemento subview
description: Elemento subview
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Capas do Windows Media Player, elemento subview
- elemento skins, subview
- Elemento subview
- referência para capas, elemento subview
- elementos, subexibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292654"
---
# <a name="subview-element"></a>Elemento subview

O elemento **subview** fornece uma maneira de manipular uma parte de uma capa, por exemplo, para fornecer um painel de controle que pode ser ocultado quando não está sendo usado. Os elementos de **subexibição** são sempre filhos dos elementos de **exibição** pai e podem conter outro elemento de capa, exceto para **exibição**, **tema** e outros elementos de **subexibição** .

O elemento **subview** dá suporte aos seguintes atributos, que são definidos no elemento **View** .



| Atributo                                                       | Descrição                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)                     | Especifica ou recupera a cor da tela de fundo do controle de **subexibição** . O valor padrão é "None".        |
| [backgroundImage](view-backgroundimage.md)                     | Especifica ou recupera a imagem de plano de fundo do controle de **subexibição** .                                     |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Especifica ou recupera a quantidade pela qual o matiz da imagem de plano de fundo é deslocado.                      |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Especifica ou recupera o valor de saturação da imagem de plano de fundo.                                        |
| [backgroundTiled](view-backgroundtiled.md)                     | Especifica ou recupera um valor que indica se a imagem de plano de fundo do controle de **subexibição** está lado a lado. |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Especifica ou recupera um valor que indica se a imagem de plano de fundo pode ser redimensionada.                      |
| [transparencyColor](view-transparencycolor.md)                 | Especifica ou recupera a cor de transparência da imagem de plano de fundo.                                      |



 

O elemento **subview** oferece suporte aos atributos de ambiente, exceto quando indicado. Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md).

O elemento **subview** pode implementar os seguintes manipuladores de eventos de ambiente: [onendmove](onendmove.md) e [OnResize](onresize.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 




