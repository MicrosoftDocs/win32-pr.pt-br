---
title: Atributos da lista de reprodução
description: Atributos da lista de reprodução
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, atributos
- listas de reprodução de metarquivo, atributos
- Listas de reprodução do metarquivo do Windows Media, atributos
- atributos, listas de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916142"
---
# <a name="playlist-attributes"></a>Atributos da lista de reprodução

As listas de reprodução têm informações de metadados chamadas atributos, assim como os itens de mídia têm atributos. Você pode recuperar os nomes e valores dos atributos da lista de reprodução e exibi-los em sua interface do usuário, ou o código pode executar ações com base no valor de um atributo.

As listas de reprodução são definidas em arquivos organizados em um formato XML e determinados elementos no arquivo definem atributos de playlist. Alguns elementos de atributo são bem conhecidos; o autor do metarquivo também pode definir atributos arbitrários. Para obter mais informações sobre elementos de atributo em arquivos de playlist, consulte [Recuperando metadados](retrieving-metadata.md).

A biblioteca pode fornecer atributos adicionais de playlist, como **SourceURL** ou **UserLastPlayedTime**. Para obter mais informações sobre os atributos da lista de reprodução da biblioteca, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.

A *lista de reprodução*. a propriedade **attributeCount** recupera o número de atributos associados à playlist. A *lista de reprodução*. a propriedade **AttributeName** recupera o nome de um atributo com base em seu índice e na *lista de reprodução*. o método **getItemInfo** recupera o valor de um atributo com base em seu nome.

Você pode modificar o valor de um atributo da playlist atual com a *lista de reprodução*. método **setItemInfo** .

Um uso especial do método **setItemInfo** é classificar os itens na lista de reprodução, usando o atributo **SortAttribute** . O exemplo de C# a seguir classifica uma lista de reprodução pelos valores do atributo **UserLastPlayedTime** . A *playlist* de variável é uma referência a um objeto de **playlist** .


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



O código de exemplo C# a seguir demonstra a recuperação de atributos de playlist. A primeira função, implaylists, popula um controle ListBox com os nomes das listas de reprodução disponíveis. A segunda parte é o manipulador de eventos da caixa de listagem. Quando o usuário clica em um nome de playlist, esse código recupera os atributos dessa lista de reprodução e exibe esses atributos em uma segunda caixa de listagem.


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



O evento SelectedIndexchanged para o controle ListBox é chamado cada vez que o usuário seleciona um nome de lista de reprodução. O manipulador de eventos a seguir preenche uma segunda caixa de listagem com os nomes e valores de atributo correspondentes à seleção do usuário.


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> <dt>

[**Atributos de item de mídia**](media-item-attributes.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> </dl>

 

 




