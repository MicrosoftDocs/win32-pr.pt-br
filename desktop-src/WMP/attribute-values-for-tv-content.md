---
title: Valores de atributo para conteúdo de TV
description: Valores de atributo para conteúdo de TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
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
- atributos, conteúdo de TV
- Valores de atributo de conteúdo de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96f855d90fe0b65c4e9483dcb2ba4ae3ff7be049f1346f1038097789b2126c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583027"
---
# <a name="attribute-values-for-tv-content"></a>Valores de atributo para conteúdo de TV

Ao longo deste tópico, o **objeto Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Windows Media Player 10 ou posterior pode organizar o conteúdo da TV na biblioteca. Windows Media Player trata o conteúdo da TV como uma subcategoria de conteúdo de vídeo. Para fazer com que o conteúdo de vídeo apareça nos nós de TV na biblioteca, de definir os atributos **WM/MediaClassPrimaryID** e **WM/MediaClassSecondaryID** para os valores na tabela a seguir usando a *mídia*. **Método setItemInfo:**



| Atributo                    | Valor                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

Você também pode usar esses valores para determinar se um item de mídia digital específico contém conteúdo de TV usando a *mídia*. **getItemInfo ou** *mídia*. **Métodos getItemInfoByType.**

Lembre-se de usar **os valores guid** como valores de cadeia de caracteres ao especificar ou recuperar esses valores. 

O código de exemplo C# a seguir define os atributos de classe de mídia para que um item de mídia seja identificado como conteúdo de TV.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Para obter mais informações sobre os valores possíveis para os atributos de classe de mídia, consulte as Diretrizes Windows uso de [metadados de mídia.](/previous-versions/ms867702(v=msdn.10))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos de item de mídia**](media-item-attributes.md)
</dt> <dt>

[**Acesso à biblioteca**](library-access.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> </dl>

 

 




