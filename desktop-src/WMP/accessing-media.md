---
title: Acessando mídia
description: Acessando mídia
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Windows Listas de reprodução do metarquivo de mídia, acessando mídia
- listas de reprodução, acessando mídia
- listas de reprodução de metarquivo, acesso à mídia
- Windows Playlists de metarquivo de mídia, acesso à mídia
- listas de reprodução, acesso à mídia
- listas de reprodução de metarquivo, acesso à mídia
- Windows Playlists de metarquivo de mídia, controlando a reprodução
- listas de reprodução, controlando a reprodução
- listas de reprodução de metarquivo, controlando a reprodução
- Windows Playlists de metarquivo de mídia, definindo a duração
- listas de reprodução, definindo a duração
- listas de reprodução de metarquivo, definindo duração
- Windows Media Player, acessando mídia
- Windows Media Player, acesso à mídia
- Windows Media Player, controle de reprodução
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
ms.openlocfilehash: c1a0846be4e8b9b62e424ce24d1b1800bc361c6a28f52a323c6bfa8511ae040b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956396"
---
# <a name="accessing-media"></a>Acessando mídia

Use as listas de reprodução para especificar e controlar a mídia de streaming ou os arquivos de mídia que Windows Media Player são executados.

Use o elemento **entry** para especificar um único elemento de mídia (um arquivo de mídia ou uma transmissão ao vivo) e quaisquer elementos filho (como imagens, links **moreinfo** e texto **abstrato** ). Use um elemento **ENTRYREF** para especificar uma lista de reprodução. Uma lista de reprodução pode conter um ou mais elementos de **entrada** ou **ENTRYREF** . Windows Media Player executa uma lista de reprodução iniciando com a primeira entrada e, em seguida, executando cada entrada por vez até que a lista seja concluída.

um elemento de **entrada** pode apontar para qualquer tipo de mídia que Windows Media Player possa reproduzir. Isso inclui não apenas arquivos. WMA,. wmv,. ASF e .avi, para citar alguns, mas também fluxos ao vivo. Usando uma série de elementos **entry** ou **ENTRYREF** para fazer referência ao conteúdo de mídia, você pode usar uma lista de reprodução para enviar um único fluxo que consiste em várias fontes. Os fluxos referenciados serão executados em sequência e vistos como um fluxo contínuo pelo Visualizador. por exemplo, a lista de reprodução pode conter dois elementos de **entrada** : uma introdução padrão de um arquivo de mídia Windows com uma extensão. wma e um fluxo de mídia de Windows ao vivo.

> [!Note]  
> Uma lista de reprodução não deve conter links para arquivos de mídia que tenham conteúdo criado com versões diferentes do DRM (Rights Management digital). em uma lista de reprodução de metarquivo, se houver links para arquivos de mídia com conteúdo drm versão 1 e para arquivos de mídia criados com versões posteriores do drm, Windows Media Player reproduzirá apenas o conteúdo do drm versão 1.

 

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

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metarquivo de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




