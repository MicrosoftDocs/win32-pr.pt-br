---
title: mapeando RSS feeds para Windows Gerenciador de Dispositivos propriedades de mídia
description: mapeando RSS feeds para Windows Gerenciador de Dispositivos propriedades de mídia
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Gerenciador de Dispositivos de mídia, RSS feeds
- Gerenciador de Dispositivos, RSS feeds
- Guia de programação, RSS feeds
- aplicativos de desktop, RSS feeds
- criando Windows aplicativos de mídia Gerenciador de Dispositivos, RSS feeds
- RSS feeds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355515217db31740603d5c6323ef8455da4b29ee80bec508897d2d4df5d59bde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031676"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>mapeando RSS feeds para Windows Gerenciador de Dispositivos propriedades de mídia

o Windows Media Player 11 fornece um recurso de agregador RSS que permite que os usuários armazenem conteúdo obtido de podcasts em seus computadores. Este tópico descreve os elementos XML encontrados em um RSS feed. além disso, ele mapeia esses elementos RSS para Windows Gerenciador de Dispositivos propriedades de mídia.

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



a tabela a seguir lista os elementos de canal em um RSS feed e as propriedades de Gerenciador de Dispositivos de mídia Windows correspondentes.



| Elemento Channel | Status         | propriedade Gerenciador de Dispositivos de mídia de Windows correspondente   |
|-----------------|----------------|-------------------------------------------------------|
| category        | Opcional       | [g \_ wszWMDMGenre](metadata-constants.md)             |
| nuvem           | Não se aplica | Não se aplica                                        |
| direitos autorais       | Opcional       | [g \_ wszWMDMProviderCopyright](metadata-constants.md) |
| descrição     | Obrigatório       | [g \_ wszWMDMDescription](metadata-constants.md)       |
| docs            | Não se aplica | Não se aplica                                        |
| gerador       | Não se aplica | Não se aplica                                        |
| Linguagem        | Não se aplica | Não se aplica                                        |
| lastBuildDate   | Opcional       | [g \_ wszWMDMLastModifiedDate](metadata-constants.md)  |
| link            | Obrigatório       | [g \_ wszWMDMDestinationURL](metadata-constants.md)    |
| managingEditor  | Opcional       | [g \_ wszWMDMEditor](metadata-constants.md)            |
| pubDate         | Opcional       | [g \_ wszWMDMYear](metadata-constants.md)              |
| classificação          | Não se aplica | Não se aplica                                        |
| skipDays        | Não se aplica | Não se aplica                                        |
| skipHours       | Não se aplica | Não se aplica                                        |
| textInput       | Não se aplica | Não se aplica                                        |
| título           | Obrigatório       | [g \_ wszWMDMTitle](metadata-constants.md)             |
| ttl             | Opcional       | [g \_ wszWMDMTimeToLive](metadata-constants.md)        |
| webMaster       | Opcional       | [g \_ wszWMDMWebMaster](metadata-constants.md)         |



 

A tabela a seguir lista os elementos de imagem em um RSS feed e as propriedades WMDM correspondentes.



| Elemento Image | Status   | propriedade Gerenciador de Dispositivos de mídia de Windows correspondente |
|---------------|----------|-----------------------------------------------------|
| descrição   | Opcional | [g \_ wszWMDMDescription](metadata-constants.md)     |
| altura        | Opcional | [g \_ wszWMDMHeight](metadata-constants.md)          |
| link          | Opcional | [g \_ wszWMDMDestinationURL](metadata-constants.md)  |
| título         | Opcional | [g \_ wszWMDMTitle](metadata-constants.md)           |
| url           | Opcional | [g \_ wszWMDMSourceURL](metadata-constants.md)       |
| width         | Opcional | [g \_ wszWMDMWidth](metadata-constants.md)           |



 

a tabela a seguir lista os elementos de item em um RSS feed e as propriedades de Gerenciador de Dispositivos de Windows de mídia correspondentes.



| Elemento Item | Atributo   | Status         | propriedade Gerenciador de Dispositivos de mídia de Windows correspondente            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| autor       |             | Opcional       | [g \_ wszWMDMAuthor](metadata-constants.md)                     |
| category     |             | Opcional       | [g \_ wszWMDMGenre](metadata-constants.md)                      |
|              | domínio      | Não se aplica | Não se aplica                                                 |
| descrição  |             | Opcional       | [g \_ wszWMDMDescription](metadata-constants.md)                |
| Gabinete    |             | Opcional       | Não se aplica                                                 |
|              | comprimento      | Obrigatório       | [g \_ wszWMDMFileSize](metadata-constants.md)                   |
|              | type        | Obrigatório       | (O tipo MIME deve ser mapeado para o tipo de conteúdo da propriedade.) |
|              | url         | Obrigatório       | [g \_ wszWMDMSourceURL](metadata-constants.md)                  |
| guid         |             | Opcional       | [g \_ wszWMDMediaGuid](metadata-constants.md)                   |
|              | isPermaLink | Não se aplica | Não se aplica                                                 |
| link         |             | Opcional       | [g \_ wszWMDMDestinationURL](metadata-constants.md)             |
| pubDate      |             | Opcional       | [g \_ wszWMDMYear](metadata-constants.md)                       |
| source       |             | Não se aplica | Não se aplica                                                 |
| título        |             | Opcional       | [g \_ wszWMDMTitle](metadata-constants.md)                      |



 

Exemplo

O exemplo a seguir mostra uma RSS feed para um podcast fictício fornecido pelo CEO de uma empresa de publicação.


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



Mapeamento de elementos de canal RSS para Windows mídia Gerenciador de Dispositivos propriedade property

A tabela a seguir descreve como os valores nos elementos do Canal RSS no exemplo anterior são mapeados para propriedades específicas Windows Media Gerenciador de Dispositivos.



| Windows Propriedade Gerenciador de Dispositivos mídia                    | Valor                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthorDate](metadata-constants.md)           | Sexta-feira, 9 de junho de 2006, 14:00:28 EDT                                                                 |
| [g \_ wszWMDMDESCRIPTION](metadata-constants.md)          | O CEO da Lucerne Publishing Peter Bankov dá uma olhada nas tendências mais recentes em publicações online. |
| [g \_ wszWMDMDESTINATION \_ URL](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszWMDMEDITOR](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md)     | Sexta-feira, 9 de junho de 2006, 14:00:28 EDT                                                                 |
| [g \_ wszWMDMFileName](metadata-constants.md)             | A publicação digital                                                                       |
| [g \_ wszWMDMFileSize](metadata-constants.md)             | 13,790                                                                                        |
| [g \_ wszWMDMFormatCode](metadata-constants.md)           | WMDM \_ FORMATCODE \_ MEDIA \_ CAST                                                                 |
| [g \_ wszWMDMGENRE](metadata-constants.md)                | News                                                                                          |
| [g \_ wszWMDMLAST \_ MODIFIED \_ DATE](metadata-constants.md) | Sexta-feira, 9 de junho de 2006, 14:00:28 EDT                                                                 |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md)     | Sexta-feira, 9 de junho de 2006, 14:00:28 EDT                                                                 |
| [g \_ wszWMDMProviderCopyright](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. Todos os direitos reservados.                                        |
| [g \_ wszWMDMTimeToLive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszWMDMTitle](metadata-constants.md)                | A publicação digital                                                                       |
| [g \_ wszWMDMWEBMASTER](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszWMDMYear](metadata-constants.md)                 | Sexta-feira, 9 de junho de 2006, 14:00:28 EDT                                                                 |



 

Mapeamento de elementos de imagem RSS para Windows mídia Gerenciador de Dispositivos propriedade property

A tabela a seguir descreve como os valores nos elementos da Imagem do RSS no exemplo anterior são mapeados para propriedades Windows mídia Gerenciador de Dispositivos específicas.



| Windows Propriedade Gerenciador de Dispositivos mídia                | Valor                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszWMDMAlbumCoverFormat](metadata-constants.md) | GIF DE FORMATO \_ DE \_ OBJETO \_ WPD                         |
| [g \_ wszWMDMAlbumCoverSize](metadata-constants.md)   | 512                                              |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Logotipo lucerne                                     |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszWMDMHeight](metadata-constants.md)           | 300                                              |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Lucerne Publishing                               |
| [g \_ wszWMDMWidth](metadata-constants.md)            | 300                                              |



 

Mapeamento de elementos de item RSS para Windows mídia Gerenciador de Dispositivos propriedade

A tabela a seguir descreve como os valores nos elementos do Item RSS no exemplo anterior são mapeados para propriedades Windows mídia Gerenciador de Dispositivos específicas.



| Windows Propriedade Gerenciador de Dispositivos mídia                | Valor                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthor](metadata-constants.md)           | Zulu                                                                                                                             |
| [g \_ wszWMDMAuthorDate](metadata-constants.md)       | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Publicações online estão mudando rapidamente. Um CEO da casa de publicação examina as tendências dos últimos cinco anos e suas implicações. |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMDuration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md) | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMFileSize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszWMDMFormatCode](metadata-constants.md)       | \_FORMATCODE de \_ mp3 do WMDM                                                                                                               |
| [g \_ wszWMDMGenre](metadata-constants.md)            | News                                                                                                                                |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md) | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMMediaGuid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMTitle](metadata-constants.md)            | A publicação digital                                                                                                             |
| [g \_ wszWMDMYear](metadata-constants.md)             | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes de metadados**](metadata-constants.md)
</dt> </dl>

 

 




