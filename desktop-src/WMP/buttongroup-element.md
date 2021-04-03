---
title: Elemento de botão
description: Elemento de botão
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Capas do Windows Media Player, elemento de botão
- capas, elemento de botão
- Elemento de botão
- referência de capas, elemento de botão
- elementos, um botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4de489e779b5e20214778b56fd8d19c7627e444
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084117"
---
# <a name="buttongroup-element"></a>Elemento de botão

O elemento **Button** fornece uma maneira de agrupar vários botões em uma capa. Esses botões podem ser especificados usando elementos **buttonelement** como filhos do elemento **Button** .

O elemento **Button** dá suporte aos seguintes atributos.



| Atributo                                              | Descrição                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [buttonCount](buttongroup-buttoncount.md)             | Recupera o número de botões no **botão**.                                                                                                                                                                         |
| [cursor](buttongroup-cursor.md)                       | Especifica ou recupera o tipo de cursor que aparece quando o mouse está sobre um botão no botão **.**                                                                                                                  |
| [disabledImage](buttongroup-disabledimage.md)         | Especifica ou recupera o nome da imagem que representa o estado desabilitado dos botões no **botão**.                                                                                                             |
| [downImage](buttongroup-downimage.md)                 | Especifica ou recupera o nome da imagem que representa o estado inferior do **botão**.                                                                                                                                |
| [hoverDownImage](buttongroup-hoverdownimage.md)       | Especifica ou recupera o nome da imagem que representa o estado de focalização de um botão no **botão**. O estado de focalização ocorre quando o botão está no estado inativo e o usuário passa o mouse sobre ele. |
| [hoverImage](buttongroup-hoverimage.md)               | Especifica ou recupera o nome da imagem que representa o estado de foco de um botão no **botão**. O estado de foco ocorre quando o botão está no estado ativo e o usuário passa o mouse sobre ele.             |
| [hueShift](buttongroup-hueshift.md)                   | Especifica ou recupera a quantidade pela qual o matiz das imagens de um **botão** é deslocado.                                                                                                                                    |
| [imagem](buttongroup-image.md)                         | Especifica ou recupera o nome da imagem que representa os botões de um **botão**.                                                                                                                                     |
| [mappingImage](buttongroup-mappingimage.md)           | Especifica ou recupera o nome da imagem que representa o mapa de botão do **botão**.                                                                                                                                |
| [radio](buttongroup-radio.md)                         | Especifica ou recupera um valor que indica se o **botão** é composto por botões de opção.                                                                                                                             |
| [saturação](buttongroup-saturation.md)               | Especifica ou recupera o valor de saturação das imagens de um **botão** .                                                                                                                                                      |
| [obter plano de fundo](buttongroup-showbackground.md)       | Especifica ou recupera um valor que indica se o **MyButton** exibe apenas os botões ou exibe o bitmap completo especificado no atributo **Image** .                                                              |
| [transparencyColor](buttongroup-transparencycolor.md) | Especifica ou recupera a cor transparente das imagens de um **botão** .                                                                                                                                                     |



 

O elemento **Button** dá suporte aos métodos a seguir.



| Método                                 | Descrição                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [Selecione](buttongroup-click.md)         | Chama o manipulador de eventos **onclick** definido para o **buttonelement** com o índice especificado. |
| [getbutton](buttongroup-getbutton.md) | Recupera o **botãoelement** com o índice especificado.                                       |



 

O elemento de **botão** é compatível com os atributos de ambiente e pode implementar os manipuladores de eventos de ambiente. Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




