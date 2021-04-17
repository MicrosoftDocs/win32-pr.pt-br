---
title: Sobre o Mediacollection e os objetos de mídia
description: Sobre o Mediacollection e os objetos de mídia
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player, objeto Mediacollection
- Modelo de objeto do Windows Media Player, objeto Mediacollection
- modelo de objeto, objeto Mediacollection
- Controle ActiveX do Windows Media Player, objeto Mediacollection
- Controle ActiveX, objeto Mediacollection
- Controle ActiveX móvel do Windows Media Player, objeto Mediacollection
- Windows Media Player Mobile, objeto Mediacollection
- Objeto mediacollection
- Windows Media Player, objeto de mídia
- Modelo de objeto do Windows Media Player, objeto de mídia
- modelo de objeto, objeto de mídia
- Controle ActiveX do Windows Media Player, objeto de mídia
- Controle ActiveX, objeto de mídia
- Controle ActiveX móvel do Windows Media Player, objeto de mídia
- Windows Media Player Mobile, objeto de mídia
- Objeto de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763389"
---
# <a name="about-the-mediacollection-and-media-objects"></a>Sobre o Mediacollection e os objetos de mídia

O **mediacollection** e os objetos de **mídia** regem a coleção de mídias, que define os locais de arquivos de mídia digital que o Windows Media Player pode acessar. Você Obtém o objeto **mediacollection** da propriedade **mediacollection** do objeto **Player** . A propriedade **mediacollection** retorna o objeto **mediacollection** . Você só pode acessar as propriedades do objeto **mediacollection** depois de criá-lo. Por exemplo, para adicionar um objeto de **mídia** (uma música), use o seguinte código:


```C++
player.mediacollection.add('laure.wma');

```



Você adicionou o arquivo Laure. WMA à coleção de mídia.

Você pode obter o objeto de **mídia** atual usando a propriedade **currentMedia** do **Player**. Por exemplo, esse código obtém a propriedade **Duration** do objeto de **mídia** atual:


```C++
myduration = player.currentmedia.duration;

```



Há várias maneiras de obter um objeto de **mídia** para que você possa acessar suas propriedades. Por exemplo, se você quiser acessar a propriedade **Duration** da mídia atual, cada uma das linhas de código a seguir poderá ser usada.

Para obter a duração da mídia em execução no momento:


```C++
player.currentMedia.duration;

```



Para obter a duração da mídia atual em uma lista de reprodução:


```C++
player.controls.currentItem.duration;

```



Para obter a duração do terceiro item de mídia em uma lista de reprodução:


```C++
player.currentPlaylist.item(2).duration;

```



Para obter a duração do terceiro item de mídia em um gênero "Jazz":


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



Para obter a duração do terceiro item de mídia na segunda Playlist:


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




