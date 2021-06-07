---
title: Gerenciando itens de mídia
description: Gerenciando itens de mídia
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player, biblioteca
- Windows Media Player modelo de objeto, biblioteca
- modelo de objeto, biblioteca
- Windows Media Player Mobile, biblioteca para o modelo de objeto
- Windows Media Player controle ActiveX, biblioteca para modelo de objeto
- Windows Media Player controle ActiveX Móvel, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Windows Media Player, gerenciando itens de mídia
- biblioteca, gerenciando itens de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf984c2f884ae828bd6426dd2a3f6da19a78ddea
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386885"
---
# <a name="managing-media-items"></a>Gerenciando itens de mídia

Um **objeto Media** representa um item de mídia. Ele tem propriedades e métodos que você pode usar para recuperar informações e exibi-las para o usuário ou para tomar ações diferentes com base no valor recuperado.

Grande parte do seu trabalho com **objetos de** Mídia envolve metadados sobre o conteúdo do item de mídia, chamados de atributos. O tópico [Atributos de Item de](media-item-attributes.md) Mídia descreve como ler e alterar valores de atributo. Além deste tópico, consulte as Diretrizes de uso de metadados de mídia do [Windows](/previous-versions/ms867702(v=msdn.10)) no site da Microsoft para obter mais informações sobre os atributos e seu uso.

O **objeto Media** tem propriedades e métodos que recuperam alguns atributos diretamente, como o nome ou a duração do item. Para itens de vídeo, você pode recuperar a altura e a largura da imagem e recuperar informações de marcador com base no nome ou índice de um marcador. Você também pode determinar se um item de mídia específico está incluído em uma playlist específica.

## <a name="retrieving-a-media-object"></a>Recuperando um objeto de mídia

Você pode acessar rapidamente o item de mídia atual usando o *Player*. **propriedade currentMedia.**

Ao longo deste tópico, o **objeto Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



O exemplo de C# a seguir recupera um **objeto Media** que representa o item atual.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



Você pode criar um novo item de mídia de um arquivo de mídia digital usando o *Player*. **Método newMedia.** Você passa o caminho da URL para um arquivo de mídia digital e ele retorna uma referência ao novo **objeto Media.** O método não adiciona o novo objeto à biblioteca diretamente. No entanto, você pode passar o objeto para a *Playlist*. **Método appendItem** ou *Playlist*. **Método insertItem.**

O exemplo de C# a seguir cria um objeto **Media** com base em um dos exemplos de mídia digital instalados com o SDK Windows Media Player.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> Você deve incluir dois caracteres de invertida ( ) (ou usar o caractere @ em C#) em uma cadeia de caracteres para representar um caractere de faixa \\ invertida real. Isso porque o C# usa um único caractere de faixa invertida para definir uma sequência de escape.

 

Você pode criar um novo item de mídia de um arquivo de mídia digital e adicioná-lo à biblioteca em uma etapa usando *MediaCollection*. **método add.** Como o *Player*. **método newMedia,** o **método add** leva um caminho para um arquivo de mídia digital.

O exemplo C# a seguir cria um **objeto Media** com base em um dos arquivos de exemplo do SDK e adiciona esse objeto à biblioteca.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



Você pode recuperar um objeto **Media** que representa um item de mídia em uma playlist usando a *Playlist*. **método item.** O exemplo de C# a seguir recupera o sexto item de mídia da playlist atual.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Controls.currentItem**](controls-currentitem.md)
</dt> <dt>

[**Gerenciando playlists**](managing-playlists.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Trabalhando com a biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




