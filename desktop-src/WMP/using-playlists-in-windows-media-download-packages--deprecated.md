---
title: Usando listas de reprodução em pacotes de download do Windows Media (preterido)
description: Usando listas de reprodução em pacotes de download do Windows Media (preterido)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Metaarquivos do Windows Media, pacotes de download do Windows Media
- Windows Media Player, pacotes de download do Windows Media
- metaarquivos, pacotes de download do Windows Media
- Windows Media, pacotes de download do Windows Media
- listas de reprodução, pacotes de download do Windows Media
- listas de reprodução de metarquivo, pacotes de download do Windows Media
- Listas de reprodução do metarquivo do Windows Media, pacotes de download do Windows Media
- Pacotes de download do Windows Media, playlists
- Pacotes de download do Windows Media, listas de reprodução do metarquivo
- Pacotes de download do Windows Media, playlists do metarquivo do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364258"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>Usando listas de reprodução em pacotes de download do Windows Media (preterido)

Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.

As listas de reprodução são arquivos de mídia do Windows com uma extensão de nome de arquivo. asx que fornece informações que dizem ao Windows Media Player como reproduzir o conteúdo empacotado. Ao combinar vários arquivos de conteúdo em um único pacote de download do Windows Media, você pode controlar e personalizar o pacote de download do Windows Media usando a lista de reprodução.

> [!Note]  
> Em geral, as listas de reprodução de metarquivo são usadas pelos pacotes de download de mídia do Windows para fazer referência ao conteúdo de multimídia no pacote, em vez de um fluxo de um servidor em uma intranet ou na Internet. No entanto, há suporte para referências de URL dentro do arquivo. asx.

 

Usando XML, o metarquivo fornece as informações que o Windows Media Player usa para reproduzir e exibir conteúdo. As listas de reprodução são constituídas de vários elementos de código XML com suas marcas e atributos associados. Cada elemento em uma lista de reprodução do metarquivo do Windows Media define uma configuração ou ação específica no Windows Media Player.

O computador do usuário associa um metarquivo do Windows Media que tem uma extensão de nome de arquivo. asx com o Windows Media Player. O Windows Media Player abre e analisa o código XML no metarquivo, que contém o caminho para localizar os arquivos de áudio ou vídeo empacotados. Em seguida, o script de metarquivo controla a experiência gráfica, de vídeo e de áudio. O metarquivo também contém informações que o Windows Media Player processa e exibe na caixa suspensa playlist. Imediatamente após a lista ser exibida, o primeiro item da lista é reproduzido.

Uma playlist de metarquivo é um atalho para os arquivos que contêm o conteúdo do pacote. O código a seguir é um exemplo de um metarquivo que especifica a borda a ser exibida usando o elemento **Skin** , duas músicas a serem reproduzidas e as informações da playlist para cada música.


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Bordas do Windows Media Player (preterido)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Pacotes de download do Windows Media (preterido)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Metaarquivos do Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




