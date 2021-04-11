---
title: Uma lista de reprodução de estação de rádio de exemplo
description: Uma lista de reprodução de estação de rádio de exemplo
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Listas de reprodução do metarquivo do Windows Media, exemplos de playlist
- listas de reprodução, exemplos de playlist
- listas de reprodução de metarquivo, exemplos de playlist
- Playlists do metarquivo do Windows Media, listas de reprodução de exemplo
- listas de reprodução, exemplos de listas de reprodução
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Playlists do metarquivo do Windows Media, listas de reprodução de exemplo
- listas de reprodução, listas de reprodução de exemplo
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Playlists do metarquivo do Windows Media, exemplo de código
- listas de reprodução, exemplo de código
- listas de reprodução de metarquivo, exemplo de código
- Playlists do metarquivo do Windows Media, exemplo de playlist de estação de rádio
- listas de reprodução, exemplo de playlist de estação de rádio
- listas de reprodução de metarquivo, exemplo de playlist de estação de rádio
- Exemplos do Windows Media Player, playlist
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, exemplo de playlist de estação de rádio
- exemplos de playlist
- exemplos de playlist
- listas de reprodução de exemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363878"
---
# <a name="an-example-radio-station-playlist"></a>Uma lista de reprodução de estação de rádio de exemplo

O código de exemplo a seguir ilustra como criar uma lista de reprodução para digitalizar três estações de rádio de rock. A marca de rádio da empresa fictícia Adventure Works está na lista de reprodução e em todos os fluxos individuais na lista de reprodução. Ao escrever seu código, altere todas as URLs e nomes de arquivo para nomes de arquivo válidos que sejam acessíveis ao seu Windows Media Player.

Uma playlist é criada para cada uma das estações. Uma quarta lista de reprodução examina as três primeiras. As listas de reprodução são criadas para referenciar anúncios gerados dinamicamente e ter a identidade visual de rádio da Adventure Works.

Uma das listas de reprodução que representam uma estação de rádio pode ser parecida com esta.


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



A lista de reprodução pode ser construída de referências para as listas de reprodução individuais.

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



Este exemplo deve reproduzir um anúncio seguido de 30 segundos de cada uma das três estações referenciadas, uma após a outra. Este ciclo será repetido indefinidamente porque o atributo **Count** do elemento **REPEAT** não está definido.

-   Os exemplos de empresas, organizações, produtos, pessoas e eventos aqui descritos são fictícios. Nenhuma associação com qualquer empresa, organização, produto, pessoa ou evento real é intencional nem deve ser presumida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Exemplos de playlist**](example-playlists.md)
</dt> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




