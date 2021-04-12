---
title: Listas de reprodução e o objeto Mediacollection
description: Listas de reprodução e o objeto Mediacollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, objeto Mediacollection
- listas de reprodução de metarquivo, objeto Mediacollection
- Playlists do metarquivo do Windows Media, objeto Mediacollection
- Objeto mediacollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363839"
---
# <a name="playlists-and-the-mediacollection-object"></a>Listas de reprodução e o objeto Mediacollection

O objeto **mediacollection** fornece acesso a uma variedade de listas de reprodução especiais e inclui um método para criar uma nova lista de reprodução a partir de um metarquivo.

Os métodos a seguir recuperam listas de reprodução especiais:

-   **getAll**
-   **getByAlbum**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

Como os nomes sugerem, esses métodos recuperam as listas de reprodução que contêm todos os itens de mídia na biblioteca que correspondem a determinados critérios.

Tenha cuidado para não confundir o *mediacollection*. método **getByName** com a *playlistcollection*. método **getByName** . O método **mediacollection** retorna um objeto **playlist** contendo todos os itens de mídia que têm o nome especificado. O método **playlistcollection** retorna um objeto **PlaylistArray** contendo todas as listas de reprodução que têm o nome especificado.

Você pode usar o *mediacollection*. **adicione** o método para adicionar listas de reprodução, bem como itens de mídia à biblioteca. Para adicionar uma lista de reprodução, passe o método do caminho para o metarquivo que define a lista de reprodução. O método sempre retorna um objeto de **mídia** . Não é possível converter entre os objetos de **mídia** e **playlist** . Para trabalhar com a lista de reprodução que você adicionou, recupere o objeto de **playlist** que tem o mesmo nome que o objeto de **mídia** .

O exemplo de C# a seguir demonstra como recuperar mídia por tipo usando o **mediacollection**. método **getByAttribute** . Esse código recupera os nomes de todos os atributos associados a um determinado tipo, bem como o status de leitura/gravação ou somente leitura desses atributos. Ele gera um único arquivo que contém listas de atributos para o áudio, vídeo, rádio, lista de reprodução, outros tipos de foto, música e tipo.


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



O exemplo de C# a seguir demonstra como adicionar uma lista de reprodução de um metarquivo à biblioteca.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



As listas de reprodução estáticas incluem itens de mídia específicos. As listas de reprodução automática pesquisam a biblioteca toda vez que são abertas e podem conter itens de mídia diferentes em momentos diferentes. Você pode adicionar listas de reprodução estáticas e automáticas à biblioteca usando o *mediacollection*. **Adicionar** método. Você também pode adicionar listas de reprodução estáticas usando a *playlistcollection*. método **importPlaylist** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Objeto playlistcollection**](playlistcollection-object.md)
</dt> <dt>

[**Listas de reprodução e o objeto Playlistcollection**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Listas de reprodução estáticas e automáticas**](static-and-auto-playlists.md)
</dt> </dl>

 

 




