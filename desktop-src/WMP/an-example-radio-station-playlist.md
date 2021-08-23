---
title: Um exemplo de playlist da estação de rádio
description: Um exemplo de playlist da estação de rádio
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Windows Playlists de metadados de mídia, exemplos de playlist
- playlists, exemplos de playlist
- playlists de metadados, exemplos de playlist
- Windows Playlists de metadados de mídia, playlists de exemplo
- playlists, playlists de exemplo
- playlists de metadados, playlists de exemplo
- Windows Playlists de metadados de mídia, playlists de exemplo
- playlists, playlists de exemplo
- playlists de metadados, playlists de exemplo
- Windows Playlists de metadados de mídia, exemplo de código
- playlists, exemplo de código
- playlists de metadados, exemplo de código
- Windows Playlists de metadados de mídia, exemplo de playlist de estação de rádio
- playlists, exemplo de playlist da estação de rádio
- playlists de metadados, exemplo de playlist de estação de rádio
- Windows Media Player,exemplos de playlist
- Windows Media Player, exemplos de playlists
- Windows Media Player, playlists de exemplo
- Windows Media Player, exemplo de playlist da estação de rádio
- exemplos de playlist
- exemplos de playlists
- playlists de exemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6db52d8eb9f109df870e65f79906761cfadee4a7871f4776fae3122dd93c8605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055024"
---
# <a name="an-example-radio-station-playlist"></a>Um exemplo de playlist da estação de rádio

O código de exemplo a seguir ilustra como criar uma playlist para verificar três estações de rádio de rocha. A marca Adventure Works Radio da empresa fictícia está na playlist e em todos os fluxos individuais dentro da playlist. Ao escrever seu código, altere todas as URLs e nomes de arquivo para nomes de arquivo válidos que podem ser acessados pelo Windows Media Player.

Uma playlist é criada para cada uma das estações. Uma quarta playlist examina os três primeiros. As playlists são criadas para fazer referência a anúncios gerados dinamicamente e têm a identidade visual da Adventure Works Radio.

Uma das playlists que representa uma estação de rádio pode ter esta aparência.


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



A playlist pode então ser construída de referências às playlists individuais.

Código de exemplo


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



Este exemplo reproduziria um ad seguido por 30 segundos de cada uma das três estações referenciadas, uma após a outra. Esse ciclo será repetido indefinidamente porque o **atributo COUNT** do **elemento REPEAT** não está definido.

-   Os exemplos de empresas, organizações, produtos, pessoas e eventos aqui descritos são fictícios. Nenhuma associação com qualquer empresa, organização, produto, pessoa ou evento real é intencional nem deve ser presumida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando playlists de metadados**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de exemplo**](example-playlists.md)
</dt> <dt>

[**Playlists de metadados**](metafile-playlists.md)
</dt> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metadados de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




