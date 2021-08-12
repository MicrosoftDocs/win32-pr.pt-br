---
title: Sobre os objetos MediaCollection e Media
description: Sobre os objetos MediaCollection e Media
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player, objeto MediaCollection
- Windows Media Player de objeto, objeto MediaCollection
- modelo de objeto, objeto MediaCollection
- Windows Media Player ActiveX controle, objeto MediaCollection
- ActiveX controle, objeto MediaCollection
- Windows Media Player Controle de ActiveX móvel, objeto MediaCollection
- Windows Media Player Objeto Mobile,MediaCollection
- Objeto MediaCollection
- Windows Media Player, objeto De mídia
- Windows Media Player de objeto, objeto de mídia
- modelo de objeto, Objeto de mídia
- Windows Media Player ActiveX controle,Objeto de mídia
- ActiveX controle,Objeto de mídia
- Windows Media Player Controle de ActiveX móvel, Objeto de mídia
- Windows Media Player Móvel, objeto de mídia
- Objeto de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082bea6eb3707915422a0bfa5cba63a2a999ac8df27ffa13876e74ffcfc6a882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583678"
---
# <a name="about-the-mediacollection-and-media-objects"></a>Sobre os objetos MediaCollection e Media

Os **objetos MediaCollection** e **Media** regem a coleção de mídias, que define os locais de arquivos de mídia digital que Windows Media Player podem acessar. Você obterá **o objeto MediaCollection** da **propriedade mediaCollection** do **objeto Player.** A **propriedade mediaCollection** retorna o **objeto MediaCollection.** Você só pode acessar as propriedades do **objeto MediaCollection** depois de ter criado. Por exemplo, para adicionar um **objeto Media** (uma música), use o seguinte código:


```C++
player.mediacollection.add('laure.wma');

```



Você adicionou o arquivo laure.wma à coleção de mídias.

Você pode obter o objeto **Media** atual usando a **propriedade currentMedia** do **Player**. Por exemplo, esse código obtém a **propriedade duration** do objeto **media** atual:


```C++
myduration = player.currentmedia.duration;

```



Há várias maneiras de obter um objeto **Media** para que você possa acessar suas propriedades. Por exemplo, se você quiser acessar a propriedade **duration** da mídia atual, cada uma das linhas de código a seguir poderá ser usada.

Para obter a duração da mídia atualmente em reprodução:


```C++
player.currentMedia.duration;

```



Para obter a duração da mídia atual em uma playlist:


```C++
player.controls.currentItem.duration;

```



Para obter a duração do terceiro item de mídia em uma playlist:


```C++
player.currentPlaylist.item(2).duration;

```



Para obter a duração do terceiro item de mídia em um gênero "Jazz":


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



Para obter a duração do terceiro item de mídia na segunda playlist:


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Modelo de objeto do player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




