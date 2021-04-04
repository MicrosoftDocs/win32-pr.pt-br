---
title: Gerenciando itens de mídia
description: Gerenciando itens de mídia
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, gerenciando itens de mídia
- biblioteca, gerenciando itens de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084127"
---
# <a name="managing-media-items"></a>Gerenciando itens de mídia

Um objeto de **mídia** representa um item de mídia. Ele tem propriedades e métodos que você pode usar para recuperar informações e exibi-las para o usuário, ou para executar ações diferentes com base no valor recuperado.

Grande parte do seu trabalho com objetos de **mídia** envolve metadados sobre o conteúdo do item de mídia, chamado de atributos. O tópico [atributos de item de mídia](media-item-attributes.md) descreve como ler e alterar valores de atributo. Além deste tópico, consulte as diretrizes de [uso de metadados do Windows Media](/previous-versions/ms867702(v=msdn.10)) no site da Microsoft para obter mais informações sobre os atributos e seu uso.

O objeto de **mídia** tem propriedades e métodos que recuperam alguns atributos diretamente, como o nome ou a duração do item. Para itens de vídeo, você pode recuperar a altura e a largura da imagem e pode recuperar informações de marcador com base no nome ou no índice de um marcador. Você também pode determinar se um item de mídia específico está incluído em uma determinada lista de reprodução.

## <a name="retrieving-a-media-object"></a>Recuperando um objeto de mídia

Você pode acessar rapidamente o item de mídia atual usando o *Player*. Propriedade **currentMedia** .

Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



O exemplo de C# a seguir recupera um objeto de **mídia** que representa o item atual.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



Você pode criar um novo item de mídia de um arquivo de mídia digital usando o *Player*. método **newMedia** . Você passa o método do caminho da URL para um arquivo de mídia digital e retorna uma referência ao novo objeto de **mídia** . O método não adiciona o novo objeto à biblioteca diretamente. No entanto, você pode passar o objeto para a *lista de reprodução*. método **appendItem** ou a *playlist*. método **insertItem** .

O exemplo de C# a seguir cria um objeto de **mídia** baseado em um dos exemplos de mídia digital instalados com o SDK do Windows Media Player.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> Você deve incluir duas barras invertidas ( \) caracteres (ou usar o caractere @ em C#) em uma cadeia de caracteres para representar um caractere de barra invertida real. Isso ocorre porque o C# usa um caractere de barra invertida única para definir uma sequência de escape.

 

Você pode criar um novo item de mídia de um arquivo de mídia digital e adicioná-lo à biblioteca em uma só etapa usando o *mediacollection*. **Adicionar** método. Como o *jogador*. o método **newMedia** , o método **Add** , usa um caminho para um arquivo de mídia digital.

O exemplo de C# a seguir cria um objeto de **mídia** baseado em um dos arquivos de exemplo do SDK e adiciona esse objeto à biblioteca.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



Você pode recuperar um objeto de **mídia** que representa um item de mídia em uma lista de reprodução usando a *lista de reprodução*. método de **Item** . O exemplo de C# a seguir recupera o sexto item de mídia da playlist atual.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Controls. currentItem**](controls-currentitem.md)
</dt> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Mediacollection. adicionar**](mediacollection-add.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. newMedia**](player-newmedia.md)
</dt> <dt>

[**Lista de reprodução. Item**](playlist-item.md)
</dt> <dt>

[**Trabalhando com a biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




