---
title: Alterando valores de atributo
description: Alterando valores de atributo
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Windows Media Player atributos para itens de mídia
- Windows Media Player modelo de objeto, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Dispositivo móvel, atributos para itens de mídia
- Windows Media Player ActiveX controle,atributos para itens de mídia
- Windows Media Player Controle ActiveX dispositivo móvel, atributos para itens de mídia
- ActiveX controle,atributos para itens de mídia
- Windows Media Player biblioteca, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, alterando valores
- alterando valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870d8bfa13012bd79fdd672f1543db4a484ca5d9674ef1a9e48e832119ea1b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581112"
---
# <a name="changing-attribute-values"></a>Alterando valores de atributo

Você pode alterar o valor de um atributo se sua página da Web ou aplicativo tiver acesso de leitura/gravação à biblioteca e o atributo puder ser lido e gravado.

Você pode alterar um atributo do item de mídia atual. Para alterar atributos de vários itens de mídia, você pode atribuir cada um deles por vez ao *Player*. **propriedade currentMedia.**

Ao longo deste tópico, o **objeto Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Para alterar um atributo, chame o *Player*. *currentMedia*. **Método setItemInfo,** conforme mostrado no exemplo de C# a seguir.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



Recomendamos que você chame a *Mídia*. **Método isReadOnlyItem** para determinar se você pode alterar um atributo específico.

> [!Note]  
> Se você inserir o controle em seu aplicativo, os atributos de arquivo que você alterar não serão gravados no arquivo de mídia digital até que o usuário seja executado Windows Media Player. Se você usar o controle em um aplicativo remoto escrito em C++, os atributos de arquivo que você alterar serão gravados no arquivo de mídia digital logo após você fazer as alterações. Em ambos os casos, as alterações estão imediatamente disponíveis para você por meio da biblioteca.

 

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

 

 




