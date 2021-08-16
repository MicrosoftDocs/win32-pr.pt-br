---
title: Playlists e o objeto MediaCollection
description: Playlists e o objeto MediaCollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player, playlists
- Windows Media Player modelo de objeto, playlists
- modelo de objeto, playlists
- Windows Media Player Mobile,playlists
- Windows Media Player ActiveX controle,playlists
- Windows Media Player Controle ActiveX dispositivo móvel, playlists
- ActiveX controle,playlists
- playlists, objeto MediaCollection
- playlists de metadados, objeto MediaCollection
- Windows Playlists de metadados de mídia, objeto MediaCollection
- Objeto MediaCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a0bba2e966e51523dc24965c2f2a066767b059f26a08fde9ee5856a1694df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334449"
---
# <a name="playlists-and-the-mediacollection-object"></a>Playlists e o objeto MediaCollection

O **objeto MediaCollection** fornece acesso a uma variedade de playlists especiais e inclui um método para criar uma nova playlist de um metadado.

Os seguintes métodos recuperam playlists especiais:

-   **getAll**
-   **getByAlbum**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

Como os nomes sugerem, esses métodos recuperam listas de reprodução que contêm todos os itens de mídia na biblioteca que corresponderem a determinados critérios.

Tenha cuidado para não confundir *a MediaCollection.* **Método getByName** com *PlaylistCollection*. **Método getByName.** O **método MediaCollection** retorna um **objeto Playlist** que contém todos os itens de mídia que têm o nome especificado. O **método PlaylistCollection** retorna um **objeto PlaylistArray** que contém todas as playlists que têm o nome especificado.

Você pode usar *MediaCollection*. **adicionar** método para adicionar playlists, bem como itens de mídia à biblioteca. Para adicionar uma playlist, passe o método para o metafile que define a playlist. O método sempre retorna um **objeto Media.** Não é possível fazer a cast entre **objetos de Mídia** e **Playlist.** Para trabalhar com a playlist que você adicionou, recupere o objeto **Playlist** que tem o mesmo nome que o **objeto Media.**

O exemplo de C# a seguir demonstra como recuperar mídia por tipo usando **MediaCollection**. **Método getByAttribute.** Esse código recupera os nomes de todos os atributos associados a um determinado tipo, bem como o status de leitura/gravação ou somente leitura desses atributos. Ele gera um único arquivo que contém listas de atributos para os tipos Áudio, Vídeo, Rádio, Playlist, Outros, Música e Foto.


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



O exemplo de C# a seguir demonstra como adicionar uma playlist de um metadado à biblioteca.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



As playlists estáticas incluem itens de mídia específicos. As playlists automáticas pesquisam a biblioteca sempre que são abertas e podem conter itens de mídia diferentes em momentos diferentes. Você pode adicionar playlists estáticas e automáticas à biblioteca usando *MediaCollection*. **método add.** Você também pode adicionar playlists estáticas usando *PlaylistCollection*. **Método importPlaylist.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciando playlists**](managing-playlists.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Playlists e o objeto PlaylistCollection**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Playlists estáticas e automáticas**](static-and-auto-playlists.md)
</dt> </dl>

 

 




