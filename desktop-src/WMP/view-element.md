---
title: Elemento VIEW
description: Elemento VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Windows Media Player, elemento VIEW
- skins, elemento VIEW
- Elemento VIEW
- referência para capas, elemento VIEW
- elementos, VIEW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d2b14f75d3cf5405c1663e23ad343e3c22bb2a80f60919de4505808cdf0a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571646"
---
# <a name="view-element"></a>Elemento VIEW

O **elemento VIEW** contém os detalhes da interface do usuário de uma capa e usa os atributos, métodos e manipuladores de eventos mostrados nas tabelas a seguir.

Vários **elementos VIEW** podem ser definidos como filhos do elemento **THEME** de uma capa para fornecer interfaces diferentes para diferentes situações. **Os** elementos VIEW não podem ser especificados como filhos de qualquer outro elemento e contêm todos os outros elementos de capa. Observe que cada exibição tem seu próprio escopo de variável, o que significa que ela não pode compartilhar valores de atributo com outras exibições.

O **atributo** global view pode ser usado para referenciar um elemento **VIEW** específico de qualquer lugar dentro dele. Essa é uma alternativa ao uso de seu atributo **de ID,** que deve ser usado de dentro de outros elementos **VIEW** ou de dentro do **elemento THEME.**

O **elemento VIEW** dá suporte aos atributos a seguir. Atributos marcados com um asterisco ( \* ) também são suportados pelo elemento **SUBVIEW.**



| Atributo                                                       | Descrição                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)\*                  | Especifica ou recupera a cor da tela de fundo **do VIEW** ou **SUBVIEW.**                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Especifica ou recupera a imagem de plano de fundo do **VIEW** ou **SUBVIEW.**                                             |
| [backgroundImageShift](view-backgroundimagehueshift.md)     | Especifica ou recupera a quantidade pela qual o matiz da imagem de plano de fundo é deslocado.                                  |
| [backgroundImageS saturação](view-backgroundimagesaturation.md) | Especifica ou recupera o valor de saturação da imagem de plano de fundo.                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | Especifica ou recupera um valor que indica se a imagem de plano de fundo do **VIEW** ou **SUBVIEW** está lado a lado.         |
| [category](view-category.md)                                   | Especifica ou recupera a categoria para a qual a interface do usuário será exibida.                                           |
| [focusObjectID](view-focusobjectid.md)                         | Especifica ou recupera um valor que indica qual elemento tem o foco do teclado.                                             |
| [Maxheight](view-maxheight.md)                                 | Especifica ou recupera a altura máxima do **VIEW** ao reizing.                                                |
| [maxWidth](view-maxwidth.md)                                   | Especifica ou recupera a largura máxima da **VIEW** ao reizing.                                                 |
| [Minheight](view-minheight.md)                                 | Especifica ou recupera a altura mínima do **VIEW** ao reizing.                                                |
| [Minwidth](view-minwidth.md)                                   | Especifica ou recupera a largura mínima da **VIEW** ao reizing.                                                 |
| [Redimensionável](view-resizable.md)                                 | Especifica ou recupera um valor que indica se **o VIEW** pode ser reessado.                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Especifica ou recupera um valor que indica se a imagem de plano de fundo pode ser ressada.                                  |
| [scriptFile](view-scriptfile.md)                               | Especifica os nomes de arquivo de arquivos que acompanham JScript arquivos.                                                                 |
| [timerInterval](view-timerinterval.md)                         | Especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos **ontimer.** |
| [title](view-title.md)                                         | Especifica ou recupera o título do **VIEW.** Só pode ser definido em tempo de design.                                       |
| [Titlebar](view-titlebar.md)                                   | Especifica ou recupera um valor que indica se a barra de título da janela é mostrada.                                        |
| [transparencyColor](view-transparencycolor.md)\*              | Especifica ou recupera a cor de transparência da imagem da tela de fundo.                                                  |



 

O **elemento VIEW** dá suporte aos métodos a seguir.



| Método                                              | Descrição                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Fecha a **EXIBIÇÃO**.                                       |
| [Maximizar](view-maximize.md)                       | Maximiza a **EXIBIÇÃO**.                                    |
| [Minimizar](view-minimize.md)                       | Minimiza o **VIEW.**                                    |
| [restore](view-restore.md)                         | Restaura o **VIEW.**                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | Retorna o usuário para o modo completo de Windows Media Player. |
| [size](view-size.md)                               | Resize o **VIEW** em uma borda especificada.                  |



 

O **elemento VIEW** pode implementar os manipuladores de eventos a seguir.



| Manipulador de eventos               | Descrição                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [Onclose](view-onclose.md) | Trata um evento que ocorre quando **VIEW** está prestes a ser fechado.      |
| [Onerror](view-onerror.md) | Tratará um evento de erro **se Configurações.enableErrorDialogs** estiver definido como false. |
| [Onload](view-onload.md)   | Trata um evento que ocorre quando o **VIEW** é exibido pela primeira vez.         |
| [Ontimer](view-ontimer.md) | Lida com eventos de temporizador.                                                      |



 

O **elemento VIEW** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente, exceto quando for anotou. Para obter mais informações, consulte [Atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente,](ambient-event-handlers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




