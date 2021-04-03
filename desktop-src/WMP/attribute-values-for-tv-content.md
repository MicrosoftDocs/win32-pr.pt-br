---
title: Valores de atributo para conteúdo de TV
description: Valores de atributo para conteúdo de TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
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
- atributos, conteúdo de TV
- Valores de atributo de conteúdo de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006155"
---
# <a name="attribute-values-for-tv-content"></a>Valores de atributo para conteúdo de TV

Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



O Windows Media Player 10 ou posterior pode organizar o conteúdo de TV na biblioteca. O Windows Media Player trata o conteúdo de TV como uma subcategoria de conteúdo de vídeo. Para fazer com que o conteúdo de vídeo apareça nos nós de TV na biblioteca, defina o **WM/MediaClassPrimaryID** e os atributos **WM/MediaClassSecondaryID** para os valores na tabela a seguir usando a *mídia*. método **setItemInfo** :



| Atributo                    | Valor                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

Você também pode usar esses valores para determinar se um determinado item de mídia digital contém conteúdo de TV usando a *mídia*. **getItemInfo** ou *mídia*. métodos **getItemInfoByType** .

Lembre-se de usar os valores de **GUID** como valores de **cadeia de caracteres** ao especificar ou recuperar esses valores.

O código de exemplo C# a seguir define os atributos de classe de mídia de forma que um item de mídia seja identificado como conteúdo de TV.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Para obter mais informações sobre os valores possíveis para os atributos de classe de mídia, consulte as [diretrizes de uso de metadados do Windows Media](/previous-versions/ms867702(v=msdn.10)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos de item de mídia**](media-item-attributes.md)
</dt> <dt>

[**Acesso à biblioteca**](library-access.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> </dl>

 

 




