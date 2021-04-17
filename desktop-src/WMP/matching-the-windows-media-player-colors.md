---
title: Correspondendo às cores do Windows Media Player
description: Correspondendo às cores do Windows Media Player
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Lojas online do Windows Media Player, correspondência de cores do Windows Media Player
- lojas online, correspondência de cores do Windows Media Player
- Digite 1 lojas online, correspondência de cores do Windows Media Player
- Digite 2 lojas online, correspondência de cores do Windows Media Player
- Lojas online do Windows Media Player, correspondência de cores do Windows Media Player
- lojas online, correspondência de cores do Windows Media Player
- Digite 1 lojas online, correspondência de cores do Windows Media Player
- Digite 2 lojas online, correspondência de cores do Windows Media Player
- Lojas online do Windows Media Player, correspondência de cores para o Windows Media Player
- lojas online, correspondência de cores para o Windows Media Player
- tipo 1 lojas online, correspondência de cores para o Windows Media Player
- tipo 2 lojas online, correspondência de cores para o Windows Media Player
- correspondência de cores para o Windows Media Player
- correspondência de cores do Windows Media Player
- Windows Media Player, cores correspondentes
- Windows Media Player, correspondência de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765616"
---
# <a name="matching-the-windows-media-player-colors"></a>Correspondendo às cores do Windows Media Player

Fazer com que sua página da Web da loja online corresponda ao esquema de cores do Windows Media Player é fácil. Simplesmente manipule o evento **external. OnColorChange** . Para especificar uma função para manipular o evento, use um código semelhante ao seguinte quando sua página da Web for carregada:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Cada vez que o usuário altera o esquema de cores do Windows Media Player, o Player chamará sua função. O exemplo a seguir mostra uma função simples que define o plano de fundo da página da Web para corresponder à propriedade **external. appColorLight** :


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



Também há outras propriedades de cor disponíveis para seu uso. Consulte [objeto externo para lojas online do tipo 2](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**External. appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**Evento external. OnColorChange**](external-oncolorchange-event.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




