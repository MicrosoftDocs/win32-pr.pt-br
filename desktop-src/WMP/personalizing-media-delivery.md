---
title: Personalizando a entrega de mídia
description: Personalizando a entrega de mídia
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows Playlists de metadados de mídia, personalizando a entrega de mídia
- playlists, personalizando a entrega de mídia
- listas de reprodução de metadados, personalizando a entrega de mídia
- Windows Playlists de metadados de mídia, personalização de entrega de mídia
- playlists, personalização de entrega de mídia
- playlists de metadados, personalização de entrega de mídia
- personalização de entrega de mídia
- personalizando a entrega de mídia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9483f4fc7a068c6f6456a5d170b4be73a9ba31ef85294f9a6939181dff00c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996006"
---
# <a name="personalizing-media-delivery"></a>Personalizando a entrega de mídia

Ao contrário da comunicação única que transmite conteúdo idêntico para um público-alvo em massa, o Windows Media Technologies fornece as ferramentas para usar dados demográficos para individualizar difusões. Com a Internet, a comunicação de duas vias em grande escala está prontamente disponível. Esse intercâmbio dinâmico de informações permite que os provedores de conteúdo conheçam seu público-alvo e respondam com apresentações personalizadas.

O exemplo a seguir, usando uma empresa fictícia, ilustra como a entrega de conteúdo de streaming pode ser personalizada. Esta discussão pressuém que você está familiarizado com Active Server páginas (arquivos ASP ou .asp) e definindo variáveis.

A Rede de Notícias é uma organização fictícia de notícias de difusão que expandiu suas operações para incluir um site. O principal recurso do site é uma seção em que os usuários podem criar seus próprios newscasts personalizados. Em vez de exibir um newscast tradicional destinado a um público em massa, um usuário vê um programa de notícias completo que contém apenas tópicos de interesse pessoal. A sequência a seguir descreve uma experiência típica do usuário.

1.  Um novo usuário vai para o site e clica em **Criar Seu Newscast Pessoal.**
2.  Um formulário de preferência é aberto. Nesse formulário, o usuário responde a perguntas sobre preferências pessoais, como histórias de notícias favoritas, histórias de notícias menos favoritas, contos e método comum de recebimento de notícias diárias.
3.  O usuário envia essas informações e, alguns segundos depois, visualiza um newscast completo, de 15 minutos, pessoal contendo conteúdo do programa, transições e comerciais. A seleção de cada elemento de mídia, incluindo comerciais, é baseada no perfil do usuário e é realizada automaticamente com componentes Windows Tecnologias de Mídia e ferramentas de Internet fora da plataforma.

A lista a seguir descreve como as várias ferramentas interagem para criar um newscast personalizado.

1.  O formulário de preferência que o usuário preenche é uma ASP (página Active Server) (Choices.asp). Os dados obtidos do formulário de preferência são analisados por dois componentes do servidor. Um componente usa as informações para consultar um banco de dados Microsoft SQL Server de notícias. O outro componente é um servidor de anúncios que usa um conjunto complexo de regras com base em requisitos contratuais e dados demográficos para agendar anúncios apropriados para o usuário no momento.
2.  Os dois bancos de dados retornam diferentes partes de uma playlist. O banco de dados de notícias retorna um conjunto de entradas de história apropriadas e o servidor de anúncios retorna um conjunto de entradas comerciais apropriadas.
3.  Uma segunda página do ASP (PlayShow.asp) recebe as Entradas do banco de dados de notícias e do servidor de ad e combina-as com as entradas padrão show open, close e transition. Todas as entradas são então colocadas de acordo com o modelo fornecido pelo PlayShow.asp e a página ASP retorna uma playlist para o usuário.
4.  O controle Windows Media Player inserido no computador do usuário reproduz a playlist do início ao fim e o usuário visualiza um newscast personalizado.

O exemplo a seguir é uma parte de um arquivo de playlist que um usuário pode receber. Faixas de anúncio, links MOREINFO e ABSTRACTS foram adicionados a ele.


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

[**Criando playlists de metadados**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de metadados**](metafile-playlists.md)
</dt> <dt>

[**Usando playlists de metadados**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metadados de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




