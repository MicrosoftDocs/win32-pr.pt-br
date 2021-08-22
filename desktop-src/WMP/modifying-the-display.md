---
title: Modificando a exibição
description: Modificando a exibição
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows Listas de reprodução do metarquivo de mídia, modificando exibições
- listas de reprodução, modificando exibições
- listas de reprodução de metarquivo, modificando exibições
- Windows Listas de reprodução do metarquivo de mídia, modificação de exibição
- listas de reprodução, modificação de exibição
- listas de reprodução de metarquivo, modificação de exibição
- Windows Media Player, exibir modificação
- Windows Media Player, modificando exibições
- Windows Media Player, propriedades de texto
- Windows Media Player, propriedades da imagem
- propriedades Windows Media Player, MOREINFO
- Windows Media Player, texto abstrato
- Propriedades de MOREINFO
- Texto ABSTRATO
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e18ca15f71d9d25d9c99db36683a61b52057580022805c9d5f0f0d250aa738a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054604"
---
# <a name="modifying-the-display"></a>Modificando a exibição

as listas de reprodução podem alterar o Windows Media Player interface do usuário de quatro maneiras principais:

-   Propriedades de texto
-   Propriedades da imagem
-   Propriedades de MOREINFO
-   Texto ABSTRATO

## <a name="text-properties"></a>Propriedades de texto

Windows Media Player habilita a exibição de texto de metadados de título, autor, direitos autorais e descrição. Os metadados do clipe podem vir do fluxo ou do arquivo de mídia, ou podem vir de uma lista de reprodução. Mostrar metadados vem da lista de reprodução. em geral, as listas de reprodução são um método melhor de passar propriedades de texto para Windows Media Player, especialmente se os elementos de texto provavelmente forem alterados. É mais fácil editar texto em uma lista de reprodução do que criar novamente um arquivo de mídia. E como as propriedades lidas de uma playlist substituem aquelas contidas no arquivo de mídia, você pode atualizar facilmente o texto de exibição adicionando o novo texto à propriedade correspondente em uma lista de reprodução. No exemplo a seguir, o texto dos metadados título e autor na playlist substitui o título e o texto do autor contidos no arquivo de mídia, Sample. WMA.

o texto de **descrição** é recuperado de um Windows arquivo de mídia referenciado em um elemento de **entrada** , a menos que haja um elemento **abstrato** em uma lista de reprodução de metarquivo. Se houver texto **abstrato** , ele será exibido, substituindo o texto de **Descrição** .


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a>Propriedades da imagem

As imagens de faixa podem ser adicionadas à interface do usuário do Windows Media Player. O elemento gráfico pode ser usado para anunciar, fornecer informações e fornecer acesso a sites, para citar algumas possibilidades.

Use o elemento **banner** para especificar uma imagem gráfica (32 pixels de altura por 194 pixels de largura) para exibição por Windows Media Player. O gráfico é exibido abaixo de qualquer conteúdo de vídeo. Um hiperlink pode ser adicionado à faixa usando o elemento filho **moreinfo** .

Uma dica de ferramenta pode ser definida por um elemento **abstrato** dentro do escopo do elemento de **faixa** . Qualquer texto de dica de ferramenta definido pode ser exibido pausando o ponteiro do mouse sobre o gráfico de faixa. Selecionar o gráfico de faixa com o ponteiro do mouse ativará qualquer hiperlink definido com o elemento **moreinfo** .

O formato de gráfico de **banner** preferencial é o formato GIF. O formato JPG pode ser usado se o gráfico for dimensionado corretamente.

O exemplo anterior ilustra o uso do elemento **banner** .

> [!Note]  
> não há suporte para imagens de **BANNER** com arquivos DRM ou quando Windows Media Player é inserido em uma página da web.

 

Para obter mais informações sobre faixas, consulte [gráficos personalizados no Windows Media Player](custom-graphics-in-windows-media-player.md).

## <a name="moreinfo-properties"></a>Propriedades de MOREINFO

As áreas de texto e imagem da interface do usuário podem ser associadas a URLs. Durante a reprodução, os usuários podem selecionar uma dessas seções para se conectar à URL associada a ela no navegador da Web. Por exemplo, você pode associar o site de um anunciante a uma imagem de faixa do AD, conforme mostrado no trecho de código a seguir.


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>Texto ABSTRATO

O texto **abstrato** é usado para exibir uma breve descrição de pop-up das áreas de texto ou imagem da interface do usuário à qual ele está associado. Durante a reprodução, se o ponteiro do mouse focalizar uma dessas áreas, uma dica de ferramenta aparecerá ao lado do ponteiro do mouse exibindo o texto **abstrato** associado à área. O texto **abstrato** é recuperado de um metarquivo e é definido com o elemento **abstract** . O elemento **abstract** pode ser um elemento filho de uma **entrada** ou um elemento de **faixa** .

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

 

 




