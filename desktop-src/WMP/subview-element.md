---
title: Elemento subview
description: Elemento subview
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Windows Media Player capas, elemento subview
- elemento skins, subview
- Elemento subview
- referência para capas, elemento subview
- elementos, subexibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef4f7860d1db04991a35ffeff2903e7a16a5d7bd84929313c296006f6f1c092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122906"
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

 

 




