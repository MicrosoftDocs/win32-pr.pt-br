---
title: Alterando valores de atributo
description: Alterando valores de atributo
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Windows Media Player, atributos para itens de mídia
- Modelo de objeto do Windows Media Player, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Mobile, atributos para itens de mídia
- Controle ActiveX do Windows Media Player, atributos para itens de mídia
- Controle ActiveX móvel do Windows Media Player, atributos para itens de mídia
- Controle ActiveX, atributos para itens de mídia
- Biblioteca do Windows Media Player, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, alterando valores
- alterando valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005669"
---
# <a name="changing-attribute-values"></a>Alterando valores de atributo

Você pode alterar o valor de um atributo se sua página da Web ou aplicativo tiver acesso de leitura/gravação à biblioteca e o atributo puder ser lido e gravado.

Você pode alterar um atributo do item de mídia atual. Para alterar os atributos de vários itens de mídia, você pode atribuir cada um deles por vez ao *Player*. Propriedade **currentMedia** .

Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Para alterar um atributo, chame o *Player*. *currentMedia*. método **setItemInfo** , conforme mostrado no exemplo de C# a seguir.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



Recomendamos que você chame a *mídia*. método **isReadOnlyItem** para determinar se você pode alterar um atributo específico.

> [!Note]  
> Se você inserir o controle em seu aplicativo, os atributos de arquivo alterados não serão gravados no arquivo de mídia digital até que o usuário execute o Windows Media Player. Se você usar o controle em um aplicativo remoto escrito em C++, os atributos de arquivo alterados serão gravados no arquivo de mídia digital logo depois que você fizer as alterações. Em ambos os casos, as alterações ficam imediatamente disponíveis por meio da biblioteca.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos de item de mídia**](media-item-attributes.md)
</dt> <dt>

[**Acesso à biblioteca**](library-access.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Lendo valores de atributo**](reading-attribute-values.md)
</dt> </dl>

 

 




