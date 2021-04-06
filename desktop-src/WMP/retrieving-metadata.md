---
title: Recuperando metadados
description: Recuperando metadados
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Playlists do metarquivo do Windows Media, Recuperando metadados
- listas de reprodução, Recuperando metadados
- listas de reprodução de metarquivo, Recuperando metadados
- Playlists do metarquivo do Windows Media, recuperação de metadados
- listas de reprodução, recuperação de metadados
- listas de reprodução de metarquivo, recuperação de metadados
- metadados, recuperando
- recuperando metadados
- Windows Media Player, Recuperando metadados
- Windows Media Player, recuperação de metadados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916412"
---
# <a name="retrieving-metadata"></a>Recuperando metadados

Enquanto um show ou um clipe está sendo reproduzido, o script pode recuperar metadados, como título e autor, usando os métodos **getItemInfo** dos objetos de **mídia** e **playlist** do Windows Media Player. Você pode recuperar metadados do escopo ASX usando métodos de objeto de **lista de reprodução** e do escopo de entrada usando métodos de objeto de **mídia** .

Por exemplo, para recuperar os valores de autor, resumo e PARAM no arquivo a seguir, use o método **getItemInfo** do objeto **playlist** . O nome do atributo é necessário para este método. Os nomes de atributo podem ser obtidos fornecendo o número de índice para a propriedade **AttributeName** . Os índices disponíveis para um objeto **playlist** podem ser obtidos usando a propriedade **attributeCount** .

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



Para recuperar os valores do objeto de **mídia** atual no escopo de entrada para ref, title, Copyright e param ("três"), use a propriedade **CurrentMedia** do objeto **Player** . Use a propriedade **attributeCount** do objeto de **mídia** para determinar o número de atributos disponíveis para o objeto de **mídia** especificado. Use números de índice com o método **getItemInfoByAtom** para recuperar valores de atributo. Use números de índice com o método **GetAttributeName** do objeto de **mídia** para determinar os nomes dos atributos disponíveis e, em seguida, use os resultados com o método **getItemInfo** .

Para obter um exemplo de como usar métodos de objeto do Windows Media Player para recuperar metadados, consulte [playlist. attributeCount](playlist-attributecount.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




