---
title: Acessando a biblioteca programaticamente
description: Acessando a biblioteca programaticamente
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, acessando programaticamente
- biblioteca, acessando
- Acessando a biblioteca do Windows Media Player de forma programática
- Biblioteca do Windows Media Player, adicionando itens de mídia
- biblioteca, adicionando itens de mídia
- Biblioteca do Windows Media Player, recuperando itens de mídia
- biblioteca, recuperando itens de mídia
- Biblioteca do Windows Media Player, removendo itens de mídia
- biblioteca, removendo itens de mídia
- Adicionando itens de mídia à biblioteca do Windows Media Player
- Recuperando itens de mídia da biblioteca do Windows Media Player
- removendo itens de mídia da biblioteca do Windows Media Player
- recuperando metadados
- Biblioteca do Windows Media Player, Recuperando metadados de itens de mídia
- biblioteca, Recuperando metadados de itens de mídia
- metadados, recuperando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364204"
---
# <a name="accessing-the-library-programmatically"></a>Acessando a biblioteca programaticamente

No código, a biblioteca é representada pelo objeto **mediacollection** (ou pela interface **IWMPMediaCollection** ). Os itens de mídia são representados como objetos de **mídia** (ou pela interface **IWMPMedia** ). Os itens da lista de reprodução são representados como objetos de **playlist** (ou pela interface **IWMPPlaylist** ). Para simplificar, esta seção se referirá apenas a nomes de objetos, quando possível.

Usando o objeto **mediacollection** , você pode trabalhar com itens de mídia e listas de reprodução. A biblioteca também expõe o objeto **playlistcollection** (ou a interface **IWMPPlaylistCollection** ), que fornece algumas funcionalidades específicas para trabalhar com listas de reprodução. Na maioria das vezes, o objeto **mediacollection** fornecerá a você a funcionalidade de que você precisa, mesmo ao trabalhar com listas de reprodução. Para obter mais informações sobre como trabalhar com itens de mídia, consulte [Gerenciando itens de mídia](managing-media-items.md). Para obter mais informações sobre como trabalhar com listas de reprodução, consulte [Gerenciando listas de reprodução](managing-playlists.md).

## <a name="adding-media-items-to-the-library"></a>Adicionando itens de mídia à biblioteca

Adicionar conteúdo de mídia digital à biblioteca é simples. Basta chamar o método [mediacollection. Add](mediacollection-add.md) , fornecendo o caminho para o arquivo de mídia como um argumento.

## <a name="retrieving-media-items-from-the-library"></a>Recuperando itens de mídia da biblioteca

Quando você recupera itens de mídia da biblioteca, o que você realmente recupera é uma lista de reprodução. Mesmo que você espere recuperar apenas um item de mídia, obterá um objeto de **playlist** contendo um único item, que será associado ao índice zero. Por exemplo, se você quiser recuperar um objeto de **mídia** que representa a música denominada "Jeanne", poderá usar o seguinte código JScript:


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



O código anterior recupera uma lista de reprodução que contém todos os itens de mídia com o nome "Jeanne" como o título. Para este exemplo, suponha que você saiba que há apenas uma música com esse nome na biblioteca (Observe que a biblioteca dá suporte a várias músicas com o mesmo nome). Isso significa que você pode esperar que a contagem de itens na playlist que você recuperou para igual um e o item de mídia fossem representados pelo índice zero. O código de exemplo a seguir continua o exemplo anterior para demonstrar como você recuperaria o item de mídia da lista de reprodução usando o método [playlist. Item](playlist-item.md) .


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



Para obter mais informações sobre como recuperar itens de mídia de listas de reprodução, consulte [listas de reprodução e itens de mídia](playlists-and-media-items.md) no [Guia de controle do Player](player-control-guide.md).

## <a name="retrieving-metadata-from-a-media-item"></a>Recuperando metadados de um item de mídia

Depois de recuperar um objeto de **mídia** , você pode ler os valores de atributo associados ao conteúdo. No caso mais simples, você pode simplesmente querer saber um único valor, como o nome do artista que realizou uma faixa de música. O exemplo de JScript a seguir mostra como usar o método [Media. getItemInfo](media-getiteminfo.md) para recuperar o nome do artista da mídia recuperada no exemplo anterior:


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



Um item de mídia pode ter muitos atributos diferentes, e trabalhar com metadados nem sempre é tão simples quanto o caso simples mostrado no exemplo anterior. Por exemplo, alguns atributos podem conter vários valores ou ter valores em mais de um idioma. Para obter mais informações sobre como trabalhar com metadados, consulte [atributos de item de mídia](media-item-attributes.md). Para obter mais informações sobre os vários atributos, seus significados e o suporte de tipo de arquivo, consulte a [referência de atributo](attribute-reference.md).

## <a name="removing-media-items-from-the-library"></a>Removendo itens de mídia da biblioteca

A remoção do conteúdo de mídia digital da biblioteca também é simples. Basta chamar **mediacollection. Remove**, fornecendo o objeto de **mídia** que representa o item como o primeiro argumento e o valor **true** como o segundo. O exemplo de JScript a seguir remove o arquivo chamado Jeanne (recuperado no exemplo anterior) da biblioteca:


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a biblioteca**](about-the-library.md)
</dt> <dt>

[**Sobre o Mediacollection e os objetos de mídia**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**Sobre os objetos playlist, Playlistcollection e PlaylistArray**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**Trabalhando com a biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




