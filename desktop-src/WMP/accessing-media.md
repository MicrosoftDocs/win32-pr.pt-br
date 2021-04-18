---
title: Acessando mídia
description: Acessando mídia
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Playlists do metarquivo do Windows Media, acessando mídia
- listas de reprodução, acessando mídia
- listas de reprodução de metarquivo, acesso à mídia
- Playlists do metarquivo do Windows Media, acesso à mídia
- listas de reprodução, acesso à mídia
- listas de reprodução de metarquivo, acesso à mídia
- Playlists do metarquivo do Windows Media, controlando a reprodução
- listas de reprodução, controlando a reprodução
- listas de reprodução de metarquivo, controlando a reprodução
- Playlists do metarquivo do Windows Media, definindo a duração
- listas de reprodução, definindo a duração
- listas de reprodução de metarquivo, definindo duração
- Windows Media Player, acessando mídia
- Windows Media Player, acesso à mídia
- Windows Media Player, controlando a reprodução
- Windows Media Player, definindo a duração
- Acessando mídia
- acesso à mídia
- controlando a reprodução
- definindo a duração
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105794532"
---
# <a name="accessing-media"></a>Acessando mídia

Use as listas de reprodução para especificar e controlar a mídia de streaming ou os arquivos de mídia que o Windows Media Player reproduz.

Use o elemento **entry** para especificar um único elemento de mídia (um arquivo de mídia ou uma transmissão ao vivo) e quaisquer elementos filho (como imagens, links **moreinfo** e texto **abstrato** ). Use um elemento **ENTRYREF** para especificar uma lista de reprodução. Uma lista de reprodução pode conter um ou mais elementos de **entrada** ou **ENTRYREF** . O Windows Media Player executa uma lista de reprodução iniciando com a primeira entrada e, em seguida, executando cada entrada por vez até que a lista seja concluída.

Um elemento de **entrada** pode apontar para qualquer tipo de mídia que o Windows Media Player possa reproduzir. Isso inclui não apenas arquivos. WMA,. wmv,. ASF e. avi, para citar alguns, mas também fluxos ao vivo. Usando uma série de elementos **entry** ou **ENTRYREF** para fazer referência ao conteúdo de mídia, você pode usar uma lista de reprodução para enviar um único fluxo que consiste em várias fontes. Os fluxos referenciados serão executados em sequência e vistos como um fluxo contínuo pelo Visualizador. Por exemplo, a lista de reprodução pode conter dois elementos de **entrada** : uma introdução padrão de um arquivo de mídia do Windows com uma extensão. WMA e um fluxo do Windows Media ao vivo.

> [!Note]  
> Uma lista de reprodução não deve conter links para arquivos de mídia que tenham conteúdo criado com versões diferentes do DRM (Rights Management digital). Em uma lista de reprodução de metarquivo, se houver links para arquivos de mídia com conteúdo DRM versão 1 e para arquivos de mídia criados com versões posteriores do DRM, o Windows Media Player só executará o conteúdo do DRM versão 1.

 

## <a name="controlling-playback"></a>Controlando a reprodução

Use as listas de reprodução para controlar não apenas quais clipes de mídia são reproduzidos, mas também quais partes do clipe são reproduzidas e como. Você pode usar as listas de reprodução para definir um conjunto de clipes a serem em loop ou repetidos, para definir a duração da reprodução e para atribuir horários de início e marcadores de início e término para cada entrada. Os elementos **StartTime**, **STARTMARKER** e **endmarcer** funcionam em conjunto com marcadores no arquivo de mídia.

Por exemplo, a lista de reprodução a seguir usa uma faixa de anúncio e o link **moreinfo** associado em uma **entrada** e faz referência a um **STARTMARKER** e um **endmarcer**.


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a>Definindo a duração

Use o elemento **Duration** para especificar por quanto tempo reproduzir um clipe ou conjunto de clipes. Você também pode usar o atributo **PREviewmode** do elemento **ASX** em conjunto com o elemento **PREVIEWDURATION** para especificar por quanto tempo um clipe ou conjunto de clipes deve ser reproduzido. Defina o atributo **PREviewmode** como Sim para usar o elemento **PREVIEWDURATION** para especificar por quanto tempo o clipe associado será reproduzido. Os elementos **PREVIEWDURATION** e **Duration** têm o mesmo comportamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Usando listas de reprodução de metarquivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




