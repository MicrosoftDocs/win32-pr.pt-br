---
title: Recuperando metadados
description: Recuperando metadados
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Windows Playlists de metadados de mídia, recuperando metadados
- playlists, recuperando metadados
- playlists de metadados, recuperando metadados
- Windows Playlists de metadados de mídia, recuperação de metadados
- playlists, recuperação de metadados
- playlists de metadados, recuperação de metadados
- metadados, recuperando
- recuperando metadados
- Windows Media Player, recuperando metadados
- Windows Media Player, recuperação de metadados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aad75f6d35108a21b772c58d0b7a0fed9b22b5247f829988ec6e9403e0fec561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833623"
---
# <a name="retrieving-metadata"></a>Recuperando metadados

Enquanto um show ou clip está em reprodução, seu script pode recuperar metadados, como título e autor, usando os métodos **getItemInfo** dos objetos Windows Media Player **Mídia** e **Playlist.** Você pode recuperar metadados do escopo ASX usando métodos de objeto **Playlist** e do escopo ENTRY usando **métodos de** objeto media.

Por exemplo, para recuperar os valores de AUTHOR, ABSTRACT e PARAM no arquivo a seguir, use o **método getItemInfo** do objeto **Playlist.** O nome do atributo é necessário para esse método. Os nomes de atributo podem ser obtidos fornecendo o número de índice para a **propriedade attributeName.** Os índices disponíveis para um objeto **Playlist** podem ser obtidos usando a **propriedade attributeCount.**

## <a name="example-code"></a>Código de exemplo


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



Para recuperar os valores  do objeto Media atual no escopo ENTRY para REF, TITLE, COPYRIGHT e PARAM ("três"), use a propriedade **currentMedia** do **objeto Player.** Use a **propriedade attributeCount** do **objeto Media** para determinar o número de atributos disponíveis para o objeto **Media** especificado. Use números de índice com o **método getItemInfoByAtom** para recuperar valores de atributo. Use números de índice com o método **getAttributeName** do objeto **Media** para determinar os nomes dos atributos disponíveis e, em seguida, use os resultados com o **método getItemInfo.**

Para obter um exemplo de como usar Windows Media Player de objeto para recuperar metadados, consulte [Playlist.attributeCount](playlist-attributecount.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando playlists de metadados**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de metadados**](metafile-playlists.md)
</dt> <dt>

[**Windows Guia de metadados de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




