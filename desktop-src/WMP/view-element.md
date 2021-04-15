---
title: Elemento VIEW
description: Elemento VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Capas do Windows Media Player, elemento VIEW
- aparência, elemento VIEW
- Elemento VIEW
- referência para capas, elemento VIEW
- elementos, exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364126"
---
# <a name="view-element"></a>Elemento VIEW

O elemento **View** contém os detalhes da interface do usuário de uma capa e usa os atributos, métodos e manipuladores de eventos mostrados nas tabelas a seguir.

Vários elementos **View** podem ser definidos como filhos do elemento **Theme** de uma capa para fornecer interfaces diferentes para situações diferentes. Os elementos de **exibição** não podem ser especificados como filhos de qualquer outro elemento e contêm todos os outros elementos de capa. Observe que cada exibição tem seu próprio escopo de variável, o que significa que não é possível compartilhar valores de atributo com outras exibições.

O atributo global **View** pode ser usado para fazer referência a um elemento **View** específico de qualquer lugar dentro dele. Essa é uma alternativa ao uso de seu atributo de **ID** , que deve ser usado de dentro de outros elementos de **exibição** ou de dentro do elemento **Theme** .

O elemento **View** oferece suporte aos seguintes atributos. Os atributos marcados com um asterisco ( \* ) também têm suporte no elemento **subview** .



| Atributo                                                       | Descrição                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)\*                  | Especifica ou recupera a cor da tela de fundo da **exibição** ou da **subexibição**.                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Especifica ou recupera a imagem de plano de fundo da **exibição** ou da **subexibição**.                                             |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Especifica ou recupera a quantidade pela qual o matiz da imagem de plano de fundo é deslocado.                                  |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Especifica ou recupera o valor de saturação da imagem de plano de fundo.                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | Especifica ou recupera um valor que indica se a imagem de plano de fundo do **modo de exibição** ou da **subexibição** é colocada em ladrilho.         |
| [category](view-category.md)                                   | Especifica ou recupera a categoria para a qual a interface do usuário será exibida.                                           |
| [focusObjectID](view-focusobjectid.md)                         | Especifica ou recupera um valor que indica qual elemento tem o foco do teclado.                                             |
| [maxHeight](view-maxheight.md)                                 | Especifica ou recupera a altura máxima da **exibição** durante o redimensionamento.                                                |
| [maxWidth](view-maxwidth.md)                                   | Especifica ou recupera a largura máxima da **exibição** ao redimensionar.                                                 |
| [minHeight](view-minheight.md)                                 | Especifica ou recupera a altura mínima da **exibição** ao redimensionar.                                                |
| [minWidth](view-minwidth.md)                                   | Especifica ou recupera a largura mínima da **exibição** ao redimensionar.                                                 |
| [redimensionável](view-resizable.md)                                 | Especifica ou recupera um valor que indica se a **exibição** pode ser redimensionada.                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Especifica ou recupera um valor que indica se a imagem de plano de fundo pode ser redimensionada.                                  |
| [scriptFile](view-scriptfile.md)                               | Especifica os nomes de arquivo do que acompanham arquivos JScript.                                                                 |
| [IntervaloDoCronômetro](view-timerinterval.md)                         | Especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos **OnTimer** . |
| [title](view-title.md)                                         | Especifica ou recupera o título da **exibição**. Só pode ser definido em tempo de design.                                       |
| [titleBar](view-titlebar.md)                                   | Especifica ou recupera um valor que indica se a barra de título da janela é mostrada.                                        |
| [transparencyColor](view-transparencycolor.md)\*              | Especifica ou recupera a cor de transparência da imagem de plano de fundo.                                                  |



 

O elemento **View** oferece suporte aos métodos a seguir.



| Método                                              | Descrição                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Fecha a **exibição**.                                       |
| [tirar](view-maximize.md)                       | Maximiza a **exibição**.                                    |
| [maximiza](view-minimize.md)                       | Minimiza a **exibição**.                                    |
| [restore](view-restore.md)                         | Restaura a **exibição**.                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | Retorna o usuário para o modo completo do Windows Media Player. |
| [size](view-size.md)                               | Redimensiona a **exibição** em uma borda especificada.                  |



 

O elemento **View** pode implementar os manipuladores de eventos a seguir.



| Manipulador de eventos               | Descrição                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [fechamento](view-onclose.md) | Manipula um evento que ocorre quando a **exibição** está prestes a ser fechada.      |
| [OnError](view-onerror.md) | Manipulará um evento de erro se **Settings. enableErrorDialogs** for definido como false. |
| [carregamento](view-onload.md)   | Manipula um evento que ocorre quando a **exibição** é exibida pela primeira vez.         |
| [OnTimer](view-ontimer.md) | Manipula eventos de temporizador.                                                      |



 

O elemento **View** oferece suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente, exceto quando indicado. Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md),

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




