---
title: Mapeando RSS feeds para propriedades do Windows Media Gerenciador de Dispositivos
description: Mapeando RSS feeds para propriedades do Windows Media Gerenciador de Dispositivos
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media Gerenciador de Dispositivos, RSS feeds
- Gerenciador de Dispositivos, RSS feeds
- Guia de programação, RSS feeds
- aplicativos de desktop, RSS feeds
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, RSS feeds
- RSS feeds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822346"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>Mapeando RSS feeds para propriedades do Windows Media Gerenciador de Dispositivos

O Windows Media Player 11 fornece um recurso de agregador RSS que permite que os usuários armazenem conteúdo obtido de podcasts em seus computadores. Este tópico descreve os elementos XML encontrados em um RSS feed. Além disso, ele mapeia esses elementos RSS para as propriedades do Windows Media Gerenciador de Dispositivos.

Os elementos em um RSS feed têm a seguinte hierarquia e atributos:


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



A tabela a seguir lista os elementos de canal em um RSS feed e as propriedades correspondentes do Windows Media Gerenciador de Dispositivos.



| Elemento Channel | Status         | Propriedade Gerenciador de Dispositivos de mídia do Windows correspondente   |
|-----------------|----------------|-------------------------------------------------------|
| category        | Opcional       | [g \_ wszWMDMGenre](metadata-constants.md)             |
| nuvem           | Não aplicável | Não aplicável                                        |
| direitos autorais       | Opcional       | [g \_ wszWMDMProviderCopyright](metadata-constants.md) |
| descrição     | Obrigatório       | [g \_ wszWMDMDescription](metadata-constants.md)       |
| docs            | Não aplicável | Não aplicável                                        |
| gerador       | Não aplicável | Não aplicável                                        |
| Linguagem        | Não aplicável | Não aplicável                                        |
| lastBuildDate   | Opcional       | [g \_ wszWMDMLastModifiedDate](metadata-constants.md)  |
| link            | Obrigatório       | [g \_ wszWMDMDestinationURL](metadata-constants.md)    |
| managingEditor  | Opcional       | [g \_ wszWMDMEditor](metadata-constants.md)            |
| pubDate         | Opcional       | [g \_ wszWMDMYear](metadata-constants.md)              |
| classificação          | Não aplicável | Não aplicável                                        |
| skipDays        | Não aplicável | Não aplicável                                        |
| skipHours       | Não aplicável | Não aplicável                                        |
| textInput       | Não aplicável | Não aplicável                                        |
| título           | Obrigatório       | [g \_ wszWMDMTitle](metadata-constants.md)             |
| ttl             | Opcional       | [g \_ wszWMDMTimeToLive](metadata-constants.md)        |
| webMaster       | Opcional       | [g \_ wszWMDMWebMaster](metadata-constants.md)         |



 

A tabela a seguir lista os elementos de imagem em um RSS feed e as propriedades WMDM correspondentes.



| Elemento Image | Status   | Propriedade Gerenciador de Dispositivos de mídia do Windows correspondente |
|---------------|----------|-----------------------------------------------------|
| descrição   | Opcional | [g \_ wszWMDMDescription](metadata-constants.md)     |
| altura        | Opcional | [g \_ wszWMDMHeight](metadata-constants.md)          |
| link          | Opcional | [g \_ wszWMDMDestinationURL](metadata-constants.md)  |
| título         | Opcional | [g \_ wszWMDMTitle](metadata-constants.md)           |
| url           | Opcional | [g \_ wszWMDMSourceURL](metadata-constants.md)       |
| width         | Opcional | [g \_ wszWMDMWidth](metadata-constants.md)           |



 

A tabela a seguir lista os elementos de item em um RSS feed e as propriedades correspondentes do Windows Media Gerenciador de Dispositivos.



| Elemento Item | Atributo   | Status         | Propriedade Gerenciador de Dispositivos de mídia do Windows correspondente            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| autor       |             | Opcional       | [g \_ wszWMDMAuthor](metadata-constants.md)                     |
| category     |             | Opcional       | [g \_ wszWMDMGenre](metadata-constants.md)                      |
|              | domínio      | Não aplicável | Não aplicável                                                 |
| descrição  |             | Opcional       | [g \_ wszWMDMDescription](metadata-constants.md)                |
| SPE    |             | Opcional       | Não aplicável                                                 |
|              | comprimento      | Obrigatório       | [g \_ wszWMDMFileSize](metadata-constants.md)                   |
|              | type        | Obrigatório       | (O tipo MIME deve ser mapeado para o tipo de conteúdo da propriedade.) |
|              | url         | Obrigatório       | [g \_ wszWMDMSourceURL](metadata-constants.md)                  |
| guid         |             | Opcional       | [g \_ wszWMDMediaGuid](metadata-constants.md)                   |
|              | IsLink permanente | Não aplicável | Não aplicável                                                 |
| link         |             | Opcional       | [g \_ wszWMDMDestinationURL](metadata-constants.md)             |
| pubDate      |             | Opcional       | [g \_ wszWMDMYear](metadata-constants.md)                       |
| source       |             | Não aplicável | Não aplicável                                                 |
| título        |             | Opcional       | [g \_ wszWMDMTitle](metadata-constants.md)                      |



 

Exemplo

O exemplo a seguir mostra um RSS feed completo para um podcast fictício fornecido pelo CEO de uma empresa de publicação.


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



Mapeamento de elementos de canal RSS para os valores de Propriedade do Windows Media Gerenciador de Dispositivos

A tabela a seguir descreve como os valores nos elementos do canal RSS no exemplo anterior são mapeados para as propriedades específicas do Windows Media Gerenciador de Dispositivos.



| Propriedade Gerenciador de Dispositivos do Windows Media                    | Valor                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthorDate](metadata-constants.md)           | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMDESCRIPTION](metadata-constants.md)          | A Lucerne Publishing CEO Peter Bankov analisa as tendências mais recentes em publicações online. |
| [\_URL g wszWMDMDESTINATION \_](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszWMDMEDITOR](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md)     | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMFileName](metadata-constants.md)             | A publicação digital                                                                       |
| [g \_ wszWMDMFileSize](metadata-constants.md)             | 13.790                                                                                        |
| [g \_ wszWMDMFormatCode](metadata-constants.md)           | conversão de mídia do WMDM \_ FORMATCODE \_ \_                                                                 |
| [g \_ wszWMDMGENRE](metadata-constants.md)                | Notícias                                                                                          |
| [Data de modificação de g \_ wszWMDMLAST \_ \_](metadata-constants.md) | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md)     | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMProviderCopyright](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. Todos os direitos reservados.                                        |
| [g \_ wszWMDMTimeToLive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszWMDMTitle](metadata-constants.md)                | A publicação digital                                                                       |
| [g \_ wszWMDMWEBMASTER](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszWMDMYear](metadata-constants.md)                 | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |



 

Mapeamento de elementos de imagem RSS para os valores de Propriedade do Windows Media Gerenciador de Dispositivos

A tabela a seguir descreve como os valores nos elementos da imagem RSS no exemplo anterior são mapeados para as propriedades específicas do Windows Media Gerenciador de Dispositivos.



| Propriedade Gerenciador de Dispositivos do Windows Media                | Valor                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszWMDMAlbumCoverFormat](metadata-constants.md) | \_GIF de \_ formato de objeto WPD \_                         |
| [g \_ wszWMDMAlbumCoverSize](metadata-constants.md)   | 512                                              |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Logotipo da Lucerne                                     |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszWMDMHeight](metadata-constants.md)           | 300                                              |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Publicação na editora                               |
| [g \_ wszWMDMWidth](metadata-constants.md)            | 300                                              |



 

Mapeamento de elementos de item RSS para os valores de Propriedade do Windows Media Gerenciador de Dispositivos

A tabela a seguir descreve como os valores nos elementos de item RSS no exemplo anterior são mapeados para as propriedades específicas do Windows Media Gerenciador de Dispositivos.



| Propriedade Gerenciador de Dispositivos do Windows Media                | Valor                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthor](metadata-constants.md)           | Zulu                                                                                                                             |
| [g \_ wszWMDMAuthorDate](metadata-constants.md)       | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Publicações online estão mudando rapidamente. Um CEO da casa de publicação examina as tendências dos últimos cinco anos e suas implicações. |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMDuration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md) | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMFileSize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszWMDMFormatCode](metadata-constants.md)       | \_FORMATCODE de \_ mp3 do WMDM                                                                                                               |
| [g \_ wszWMDMGenre](metadata-constants.md)            | Notícias                                                                                                                                |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md) | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMMediaGuid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMTitle](metadata-constants.md)            | A publicação digital                                                                                                             |
| [g \_ wszWMDMYear](metadata-constants.md)             | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes de metadados**](metadata-constants.md)
</dt> </dl>

 

 




