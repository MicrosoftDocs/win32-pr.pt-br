---
title: Playlists
description: Playlists
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player, playlists
- Windows Media Player modelo de objeto, playlists
- modelo de objeto, playlists
- Windows Media Player ActiveX controle,playlists
- ActiveX controle,playlists
- Windows Media Player Controle ActiveX dispositivo móvel, playlists
- Windows Media Player Mobile,playlists
- playlists, migração
- Windows Playlists de metadados de mídia, migração
- playlists de metadados, migração
- guia de migração, playlists
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccdd98789de6c8d4faa06882376967298646febabd790067710dc4f460ba65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334468"
---
# <a name="playlists"></a>Playlists

O modelo Windows Media Player objeto de controle ActiveX 6.4 inclui quatro métodos e uma propriedade para trabalhar com playlists de metadados Windows Mídia:

-   *Player6*. **GetCurrentEntry**
-   *Player6*. **SetCurrentEntry**
-   *Player6*. **GetMediaParameter**
-   *Player6*. **GetMediaParameterName**
-   *Player6*. **EntryCount.**

Juntos, eles fornecem funcionalidade limitada para navegar por um metarquivo de playlist com uma extensão de nome de arquivo .asx e recuperar informações sobre as entradas contidas na playlist.

Windows Media Player 7 introduziu a "Biblioteca de Mídia". A biblioteca permite que os usuários organizem seu conteúdo de mídia digital, bem como criem playlists personalizadas que podem ser gerenciadas na interface gráfica do usuário do Player. O modelo de objeto de controle Windows Media Player Windows Media Player 7 ou ActiveX posterior fornece suporte para trabalhar com playlists de biblioteca, bem como playlists contidas em metadados de mídia do Windows com uma extensão de nome de arquivo .asx.

> [!Note]  
> Por motivos de segurança, o usuário deve conceder direitos de acesso à biblioteca antes que seu programa possa manipular seu conteúdo. Os direitos de acesso só podem ser solicitados e concedidos por meio do modelo de objeto Windows Media Player Série 9 ou posterior. Para obter detalhes sobre direitos de acesso, consulte [Acesso à biblioteca.](library-access.md)

 

O Windows Media Player modelo de objeto 7 ou posterior inclui três objetos para lidar com playlists. O **objeto PlaylistCollection** fornece funcionalidade para organizar playlists; ele representa toda a coleção de playlists na biblioteca do usuário. O **objeto PlaylistArray** fornece uma maneira de recuperar uma playlist específica do objeto **PlaylistCollection** usando um número de índice; dois dos métodos **de objeto PlaylistCollection** recuperam um **objeto PlaylistArray.** O **objeto Playlist** fornece as propriedades e os métodos necessários para manipular itens de mídia contidos em uma única playlist.

Por exemplo, como cada playlist na biblioteca tem um nome exclusivo, você pode recuperar uma playlist da biblioteca usando *PlaylistCollection*. **Método getByName:**


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



Com mais frequência, você deseja trabalhar com a playlist atual. Embora seja possível usar vários objetos de playlist, apenas um pode ser recuperado pelo *Player*. **propriedade currentPlaylist** a qualquer momento: aquela que Windows Media Player está processando nesse momento.

Quando Windows Media Player 7 ou posterior reproduz um metadado Windows Media com uma extensão de nome de arquivo .asx, ele cria primeiro um objeto **Playlist.** Em seguida, ele preenche o objeto com as informações da playlist .asx e, em seguida, torna esse objeto **playlist** a playlist atual. Isso significa que você pode usar as propriedades e os métodos associados ao objeto **Playlist** para manipular playlists .asx exatamente como você manipularia playlists na biblioteca. Por exemplo, para recuperar o número de entradas em uma playlist .asx usando o modelo de objeto versão 6.4, use o *Player6*. **Propriedade EntryCount:**


```C++
var entrycount = WMP64.EntryCount;

```



Ao usar o modelo de objeto Windows Media Player 7 ou posterior, use a *Playlist*. **propriedade count:**


```C++
var entrycount = WMP9.currentPlaylist.count;

```



Ao usar o controle versão 6.4, você pode usar o *Player6.* **Método GetCurrentEntry** para recuperar o índice da entrada atual em uma playlist .asx:


```C++
var entrynum = WMP64.GetCurrentEntry();

```



Você pode obter o mesmo resultado usando o modelo de objeto Windows Media Player 7 ou posterior no script. O exemplo JScript a seguir compara o objeto de mídia atual com cada item na playlist. Quando *Media*. **isIdentical retorna** true, uma caixa de mensagem exibe o índice do item de mídia atual.


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



Para especificar o índice da entrada atual em uma playlist .asx, use *Player6*. **SetCurrentEntry.** Os índices de entrada da playlist na versão 6.4 começam com 1, portanto, para tornar a segunda entrada em uma playlist de metadados a atual, use a seguinte sintaxe:


```C++
WMP6.SetCurrentEntry(2);

```



Os índices de entrada de playlist são baseados em zero Windows Media Player 7 ou posterior; para tornar a segunda entrada em uma playlist de metadados a atual, ao usar o modelo de objeto Windows Media Player 7 ou posterior, use a seguinte sintaxe:


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



O exemplo JScript a seguir demonstra uma função que aceita um número de índice como um parâmetro e, em seguida, torna a entrada de playlist que corresponde ao índice o item de mídia atual:


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



Windows Os metadados de mídia podem conter elementos de parâmetro personalizados, que você especifica usando a **<PARAM>** marca . Ao usar o modelo de objeto versão 6.4, você pode recuperar o nome de um parâmetro específico com o *Player6.* **Método GetMediaParameterName.** O exemplo JScript a seguir recupera o nome do primeiro parâmetro na primeira entrada de uma playlist .asx:


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



Da mesma forma, você pode recuperar o valor associado ao parâmetro usando *Player6*. **GetMediaParameter:**


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



O exemplo JScript a seguir usa o modelo de objeto Windows Media Player 7 ou posterior para recuperar o nome e o valor do parâmetro da primeira entrada em uma playlist .asx:


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



Você pode usar *PlaylistCollection*. **Método importPlaylist** para adicionar uma playlist .asx à biblioteca. Depois de importada, a playlist de metadados se torna uma playlist de biblioteca, para que você possa manipulá-la usando todas as propriedades e métodos à sua disposição. O usuário deve conceder direitos de acesso completo à biblioteca para que seu aplicativo possa usar o **método importPlaylist.**

Você pode usar *PlaylistCollection*. **getByName para** testar se existe uma playlist. Esse método sempre retorna um objeto **PlaylistArray** válido. Se a matriz de playlist recuperada contiver exatamente uma playlist, haverá uma playlist com esse nome na biblioteca. Caso contrário, a matriz de playlist não conterá nenhum objeto de playlist; isso significa que não há nenhuma playlist na biblioteca com o nome passado como um argumento para o **método getByName.** O exemplo JScript a seguir demonstra isso:


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

[**Gerenciando playlists**](managing-playlists.md)
</dt> <dt>

[**Guia de migração de modelo de objeto**](object-model-migration-guide.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> </dl>

 

 




