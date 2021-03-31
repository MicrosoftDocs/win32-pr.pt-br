---
title: Personalizando a entrega de mídia
description: Personalizando a entrega de mídia
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Playlists do metarquivo do Windows Media, personalizando a entrega de mídia
- listas de reprodução, personalizando a entrega de mídia
- listas de reprodução de metarquivo, personalizando a entrega de mídia
- Playlists do metarquivo do Windows Media, personalização de entrega de mídia
- listas de reprodução, personalização de entrega de mídia
- listas de reprodução de metarquivo, personalização de entrega de mídia
- personalização de entrega de mídia
- Personalizando a entrega de mídia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159401"
---
# <a name="personalizing-media-delivery"></a>Personalizando a entrega de mídia

Ao contrário da comunicação unidirecional que transmite conteúdo idêntico a um público em massa, as tecnologias de mídia do Windows fornecem as ferramentas para usar os dados demográficos para individualizar as difusões. Com a Internet, a comunicação bidirecional em grande escala está prontamente disponível. Esse intercâmbio dinâmico de informações permite que os provedores de conteúdo saibam seu público e respondam com apresentações personalizadas.

O exemplo a seguir, usando uma empresa fictícia, ilustra como a entrega de conteúdo de streaming pode ser personalizada. Esta discussão pressupõe que você esteja familiarizado com Active Server páginas (arquivos ASP ou. asp) e Definindo variáveis.

A rede de notícias é uma organização de notícias de difusão fictícia que expandiu suas operações para incluir um site. O principal recurso do site é uma seção em que os usuários podem criar seus próprios newscasts personalizados. Em vez de exibir um newscast tradicional destinado a um público em massa, um usuário vê um programa de notícias completo que contém apenas tópicos de interesse pessoal. A sequência a seguir descreve uma experiência de usuário típica.

1.  Um novo usuário vai para o site e clica em **criar seu newscast pessoal**.
2.  Um formulário de preferência é aberto. Neste formulário, o usuário responde às perguntas sobre as preferências pessoais, como histórias de notícias favoritas, menos histórias de notícias favoritas, Hobbies e o método habitual de receber notícias diárias.
3.  O usuário envia essas informações e alguns segundos depois exibe um newscast pessoal completo, de 15 minutos, que contém o conteúdo do programa, as transições e os negócios. A seleção de cada elemento de mídia, incluindo os comerciais, é baseada no perfil do usuário e é realizada automaticamente com os componentes das tecnologias de mídia do Windows e as ferramentas de Internet prontas.

A lista a seguir descreve como as várias ferramentas interagem para criar um newscast personalizado.

1.  O formulário de preferência que o usuário preenche é uma página de Active Server (ASP) (Choices. asp). Os dados obtidos do formulário de preferência são analisados por dois componentes de servidor. Um componente usa as informações para consultar um banco de dados Microsoft SQL Server de histórias de notícias. O outro componente é um servidor do AD que usa um conjunto complexo de regras com base em requisitos contratuais e demográficos para agendar anúncios apropriados para o usuário naquele momento.
2.  Os dois bancos de dados retornam partes diferentes de uma lista de reprodução. O banco de dados de história de notícias retorna um conjunto de entradas da história apropriadas e o servidor do AD retorna um conjunto de entradas comerciais apropriadas.
3.  Uma segunda página ASP (PlayShow. asp) recebe as entradas do banco de dados da história de notícias e do servidor do AD e combina aquelas com entradas padrão de exibição abrir, fechar e de transição. Em seguida, todas as entradas são dispostas de acordo com o modelo fornecido pelo PlayShow. asp, e a página ASP retorna uma lista de reprodução para o usuário.
4.  O controle do Windows Media Player inserido no computador do usuário reproduz a lista de reprodução do início ao fim e o usuário exibe um newscast personalizado.

O exemplo a seguir é uma parte de um arquivo de lista de reprodução que um usuário pode receber. Faixas do AD, links MOREINFO e ABSTRATOs foram adicionados a ele.


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   Os exemplos de empresas, organizações, produtos, pessoas e eventos aqui descritos são fictícios. Nenhuma associação com qualquer empresa, organização, produto, pessoa ou evento real é intencional nem deve ser presumida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Usando listas de reprodução de metarquivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




