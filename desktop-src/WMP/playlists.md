---
title: Playlists
description: Playlists
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- listas de reprodução, migração
- Listas de reprodução do metarquivo do Windows Media, migração
- listas de reprodução de metarquivo, migração
- Guia de migração, listas de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005251"
---
# <a name="playlists"></a>Playlists

O modelo de objeto de controle ActiveX do Windows Media Player 6,4 inclui quatro métodos e uma propriedade para trabalhar com as listas de reprodução do metarquivo de mídia do Windows:

-   *Player6*. **GetCurrentEntry**
-   *Player6*. **SetCurrentEntry**
-   *Player6*. **GetMediaParameter**
-   *Player6*. **GetMediaParameterName**
-   *Player6*. **EntryCount**.

Juntos, eles fornecem funcionalidade limitada para navegar em um metarquivo de playlist com uma extensão de nome de arquivo. ASX e recuperar informações sobre as entradas contidas na lista de reprodução.

O Windows Media Player 7 apresentou "biblioteca de mídia". A biblioteca permite que os usuários organizem seu conteúdo de mídia digital, bem como criem listas de reprodução personalizadas que podem ser gerenciadas na interface gráfica do usuário do Player. O modelo de objeto de controle ActiveX do Windows Media Player 7 ou posterior fornece suporte para trabalhar com playlists de biblioteca, bem como listas de reprodução contidas em metaarquivos do Windows Media com uma extensão de nome de arquivo. asx.

> [!Note]  
> Por motivos de segurança, o usuário deve conceder direitos de acesso à biblioteca antes que seu programa possa manipular seu conteúdo. Direitos de acesso só podem ser solicitados e concedidos por meio do modelo de objeto do Windows Media Player 9 Series ou posterior. Para obter detalhes sobre direitos de acesso, consulte [acesso à biblioteca](library-access.md).

 

O modelo de objeto do Windows Media Player 7 ou posterior inclui três objetos para lidar com listas de reprodução. O objeto **playlistcollection** fornece funcionalidade para organizar as listas de reprodução; Ele representa a coleção inteira de listas de reprodução na biblioteca do usuário. O objeto **PlaylistArray** fornece uma maneira de recuperar uma lista de reprodução específica do objeto **playlistcollection** usando um número de índice; dois dos métodos de objeto **playlistcollection** recuperam um objeto **PlaylistArray** . O objeto **playlist** fornece as propriedades e os métodos necessários para manipular itens de mídia contidos em uma única lista de reprodução.

Por exemplo, como cada playlist na biblioteca tem um nome exclusivo, você pode recuperar uma lista de reprodução da biblioteca usando a *playlistcollection*. método **getByName** :


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



Com mais frequência, você desejará trabalhar com a playlist atual. Embora seja possível usar vários objetos de lista de reprodução, apenas um pode ser recuperado pelo *jogador*. Propriedade **currentPlaylist** em um determinado momento: aquela que o Windows Media Player está processando naquele momento.

Quando o Windows Media Player 7 ou posterior reproduz um metarquivo do Windows Media com uma extensão de nome de arquivo. ASX, ele primeiro cria um objeto de **lista de reprodução** . Em seguida, ele preenche o objeto com as informações da lista de reprodução. ASX e, em seguida, torna esse objeto de **playlist** a playlist atual. Isso significa que você pode usar as propriedades e os métodos associados ao objeto **playlist** para manipular as listas de reprodução. asx exatamente como trataria as listas de reprodução na biblioteca. Por exemplo, para recuperar o número de entradas em uma lista de reprodução. asx usando o modelo de objeto da versão 6,4, use o *Player6*. Propriedade **EntryCount** :


```C++
var entrycount = WMP64.EntryCount;

```



Ao usar o modelo de objeto do Windows Media Player 7 ou posterior, use a *lista de reprodução*. Propriedade de **contagem** :


```C++
var entrycount = WMP9.currentPlaylist.count;

```



Ao usar o controle da versão 6,4, você pode usar o *Player6*. Método **GetCurrentEntry** para recuperar o índice da entrada atual em uma lista de reprodução. ASX:


```C++
var entrynum = WMP64.GetCurrentEntry();

```



Você pode obter o mesmo resultado usando o modelo de objeto do Windows Media Player 7 ou posterior no script. O exemplo de JScript a seguir compara o objeto de mídia atual com cada item na lista de reprodução. Quando *mídia*. **isidêntico** retorna true, uma caixa de mensagem exibe o índice do item de mídia atual.


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



Para especificar o índice da entrada atual em uma lista de reprodução. ASX, use *Player6*. **SetCurrentEntry**. Os índices de entrada de playlist na versão 6,4 começam com 1, portanto, para tornar a segunda entrada em uma lista de reprodução de metarquivo a atual, use a seguinte sintaxe:


```C++
WMP6.SetCurrentEntry(2);

```



Os índices de entrada de playlist são baseados em zero no Windows Media Player 7 ou posterior; para tornar a segunda entrada em uma lista de reprodução de metarquivo a atual, ao usar o modelo de objeto do Windows Media Player 7 ou posterior, use a seguinte sintaxe:


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



O exemplo de JScript a seguir demonstra uma função que aceita um número de índice como um parâmetro e, em seguida, torna a entrada da playlist que corresponde ao índice do item de mídia atual:


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



Os metaarquivos de mídia do Windows podem conter elementos de parâmetro personalizados, que você especifica usando a **<PARAM>** marca. Ao usar o modelo de objeto da versão 6,4, você pode recuperar o nome de um parâmetro específico com o *Player6*. Método **GetMediaParameterName** . O exemplo de JScript a seguir recupera o nome do primeiro parâmetro na primeira entrada de uma lista de reprodução. ASX:


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



Da mesma forma, você pode recuperar o valor associado ao parâmetro usando *Player6*. **GetMediaParameter**:


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



O exemplo de JScript a seguir usa o modelo de objeto do Windows Media Player 7 ou posterior para recuperar o nome e o valor do parâmetro da primeira entrada em uma lista de reprodução. ASX:


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



Você pode usar a *playlistcollection*. método **importPlaylist** para adicionar uma lista de reprodução. asx à biblioteca. Depois de importado, a lista de reprodução de metarquivo se torna uma lista de reprodução de biblioteca, para que você possa manipulá-la usando todas as propriedades e métodos à sua disposição. O usuário deve conceder direitos de acesso completo à biblioteca para que seu aplicativo possa usar o método **importPlaylist** .

Você pode usar *playlistcollection*. **getByName** para testar se existe uma lista de reprodução. Esse método sempre retorna um objeto **PlaylistArray** válido. Se a matriz de playlist recuperada contiver exatamente uma lista de reprodução, existirá uma playlist com esse nome na biblioteca. Caso contrário, a matriz de playlist não conterá nenhum objeto de playlist; Isso significa que não há nenhuma lista de reprodução na biblioteca com o nome passado como um argumento para o método **getByName** . O exemplo de JScript a seguir demonstra isso:


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> <dt>

[**Guia de migração do modelo de objeto**](object-model-migration-guide.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> </dl>

 

 




