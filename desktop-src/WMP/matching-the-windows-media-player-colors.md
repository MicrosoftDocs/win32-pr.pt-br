---
title: Correspondendo às cores Windows Media Player dados
description: Correspondendo às cores Windows Media Player dados
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player online, combinando Windows Media Player cores
- lojas online, correspondência de Windows Media Player cores
- type 1 online stores,matching Windows Media Player colors
- type 2 online stores,matching Windows Media Player colors
- Windows Media Player online, Windows Media Player de cores
- lojas online, Windows Media Player de cores
- type 1 online stores,Windows Media Player color matching
- tipo 2 lojas online, Windows Media Player de cores
- Windows Media Player online, correspondência de cores para Windows Media Player
- lojas online, correspondência de cores para Windows Media Player
- tipo 1 lojas online, correspondência de cores para Windows Media Player
- tipo 2 lojas online, correspondência de cores para Windows Media Player
- correspondência de cores para Windows Media Player
- correspondência Windows Media Player cores
- Windows Media Player, cores correspondentes
- Windows Media Player, correspondência de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3dbb7ed8b73973d35bc8ad884109c569d1c4738d038cf48f657068c5bde51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135179"
---
# <a name="matching-the-windows-media-player-colors"></a>Correspondendo às cores Windows Media Player dados

Fazer sua página da Web da loja online corresponder ao Windows Media Player de cores é fácil. Basta manipular **o evento External.OnColorChange.** Para especificar uma função para manipular o evento, use um código como o seguinte quando sua página da Web for carregada:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Sempre que o usuário altera o esquema de cores Windows Media Player, o Player chamará sua função. O exemplo a seguir mostra uma função simples que define o plano de fundo da página da Web para corresponder à **propriedade External.appColorLight:**


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



Há outras propriedades de cor disponíveis para seu uso também. Consulte [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**External.appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**Evento External.OnColorChange**](external-oncolorchange-event.md)
</dt> <dt>

[**Informações comuns às lojas online do tipo 1 e do tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




