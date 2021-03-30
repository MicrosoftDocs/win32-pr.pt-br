---
title: Listas de reprodução e itens de mídia
description: Listas de reprodução e itens de mídia
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, itens de mídia
- listas de reprodução de metarquivo, itens de mídia
- Playlists do metarquivo do Windows Media, itens de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916127"
---
# <a name="playlists-and-media-items"></a>Listas de reprodução e itens de mídia

Uma lista de reprodução é um conjunto de itens de mídia. Um objeto **playlist** pode manipular os objetos de **mídia** que representam esses itens.

## <a name="retrieving-media-items"></a>Recuperando itens de mídia

Para uma lista de reprodução existente, você pode ler a *lista de reprodução*. **contagem** de propriedade para determinar quantos itens de mídia estão na playlist, e você pode obter uma referência ao objeto de **mídia** correspondente a um item específico usando a *lista de reprodução*. Propriedade do **Item** .

O exemplo de C# a seguir recupera uma referência de objeto para um item de mídia específico. (Ao longo deste tópico, a variável *plist* é uma referência a um objeto **playlist** .)


```C++
currMedia = pList.Item(0);

```



O exemplo de C# a seguir recupera os nomes de todos os itens de mídia em uma lista de reprodução e os coloca em uma caixa de listagem chamada lstOutput.


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a>Adicionando itens a uma lista de reprodução

Você pode adicionar um item de mídia ao final de uma lista de reprodução ou a uma posição específica em uma lista de reprodução, usando a *lista de reprodução*. **appendItem** e *playlist*. métodos **insertItem** .

Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



O exemplo de C# a seguir demonstra as duas técnicas adicionando o item de mídia atual a uma lista de reprodução denominada "BluesTest", primeiro no final e, em seguida, no início da lista de reprodução.


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



Quando você cria uma nova lista de reprodução vazia usando a *playlistcollection*. método **newPlaylist** , você pode adicionar itens de mídia a ele chamando repetidamente a *lista de reprodução*. método **appendItem** .

## <a name="manipulating-media-items-in-a-playlist"></a>Manipulando itens de mídia em uma lista de reprodução

Você pode alterar a posição de um item de mídia na lista de reprodução usando a *lista de reprodução*. método **moveItem** . Você especifica o item por seu índice atual e, em seguida, especifica o novo índice. O exemplo C# a seguir move um item do índice 5 para o índice 0 em uma lista de reprodução.


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



Você pode remover um item de mídia da lista de reprodução usando a **lista de reprodução**. método **RemoveItem** . Observe que, se o item removido não for o item final na lista de reprodução, os valores de índice dos itens subsequentes mudarão. O exemplo de C# a seguir remove o item especificado.


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> Os usuários podem alterar o conteúdo de uma lista de reprodução fora do seu aplicativo. Sempre que você manipula os itens em uma lista de reprodução, deve monitorar e manipular os eventos relacionados à playlist do controle do Windows Media Player para garantir que seu código funcione corretamente. Esses eventos são *Player*. **CurrentPlaylistChange** e *Player*. **PlaylistChange**.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> </dl>

 

 




