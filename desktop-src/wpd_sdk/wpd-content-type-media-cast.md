---
description: CAST DE MÍDIA \_ DO \_ TIPO DE \_ CONTEÚDO \_ WPD
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d45c9bc1e8e41bae526f02102d341ef00fad435
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423456"
---
# <a name="wpd_content_type_media_cast"></a>CAST DE MÍDIA \_ DO \_ TIPO DE \_ CONTEÚDO \_ WPD

Um objeto que descreve seu tipo como WPD \_ CONTENT TYPE MEDIA CAST representa uma coleção de conteúdo \_ \_ \_ relacionado.

Um objeto Mediacast pode ser pensado como um objeto de contêiner que grupos de conteúdo relacionado, assim como uma música de grupos de playlists. Geralmente, um objeto Mediacast é usado para agrupar o conteúdo de mídia que foi publicado online. Por exemplo, um canal RSS pode ser representado como um objeto Mediacast cujas referências de objeto apontam para objetos de conteúdo que representam cada item no canal.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da propriedade             |  Obrigatório ou Opcional         |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                | Obrigatórios.                                                             |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                 | Obrigatórios.                                                             |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                             |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                          | Obrigatórios.                                                             |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                        | Obrigatórios.                                                             |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                           | Obrigatórios.                                                             |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                     |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                    | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema). |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                     |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                             |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo. |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.               |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                             |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                             |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                             |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                          |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                             |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                     | Recomendado se o objeto for referenciado por outro objeto.            |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                             |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                             |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                               | Necessário se o objeto puder ser excluído.                                |
| [LOCALIDADE DA \_ LINGUAGEM \_ DE OBJETO \_ WPD](object-properties.md)                                                                | Necessário se o objeto não puder ser excluído.                             |
| [DIREITOS \_ AUTORAIS DA MÍDIA WPD \_](media-properties.md)                                                     | Opcional.                                                             |
| [CLASSIFICAÇÃO DOS \_ \_ PAIS DE MÍDIA WPD \_](media-properties.md)                                        | Opcional.                                                             |
| [META-GÊNERO DE MÍDIA WPD \_ \_ \_](media-properties.md)                                                  | Opcional.                                                             |
| [SUB-TÍTULO \_ DE \_ MÍDIA \_ WPD](media-properties.md)                                                    | Opcional.                                                             |
| [WPD \_ MEDIA \_ RELEASE \_ DATE](media-properties.md)                                              | Recomendável.                                                          |
| [TÍTULO DA \_ MÍDIA \_ WPD](media-properties.md)                                                             | Recomendável.                                                          |
| [PROPRIETÁRIO DA MÍDIA WPD \_ \_](media-properties.md)                                                             | Recomendável.                                                          |
| [EDITOR DE GERENCIAMENTO DE MÍDIA WPD \_ \_ \_](media-properties.md)                                        | Recomendável.                                                          |
| [WPD \_ MEDIA \_ WEBMASTER](media-properties.md)                                                     | Recomendável.                                                          |
| [URL DE \_ ORIGEM \_ DA MÍDIA WPD \_](media-properties.md)                                                  | Recomendável.                                                          |
| [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md)                                        | Recomendável.                                                          |
| [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)                                                 | Opcional.                                                             |
| [GÊNERO DE MÍDIA WPD \_ \_](media-properties.md)                                                             | Opcional.                                                             |
| [INDICADOR DE \_ OBJETO \_ DE MÍDIA \_ WPD](media-properties.md)                                        | Recomendadas                                                           |
| [DATA DO \_ ÚLTIMO BUILD DA \_ MÍDIA \_ \_ WPD](media-properties.md)                                       | Recomendável.                                                          |
| [TEMPO DE \_ \_ VIDA DE MÍDIA \_ WPD \_](media-properties.md)                                             | Opcional.                                                             |
| [SUB DESCRIÇÃO DA MÍDIA WPD \_ \_ \_](object-properties.md)                                                                 | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os seguintes recursos.



| Nome do Recurso                                               | Obrigatório ou opcional | Descrição                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**\_padrão de recursos WPD \_**](wpd-resource-default.md)      | Opcional.            | Contém os dados do arquivo mediacast. Por exemplo, se esse mediacast representa um canal RSS, esse pode ser o documento RSS. |
| [**\_miniatura do recurso WPD \_**](wpd-resource-thumbnail.md)  | Opcional.            | Contém a miniatura que representa este mediacast.                                                                         |
| [**\_arte do \_ álbum de recursos WPD \_**](wpd-resource-album-art.md) | Opcional.            | Contém o trabalho artístico para este mediacast.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Mapeamento de elementos RSS e propriedades Mediacast

Um canal RSS pode ser representado como um objeto Mediacast cujas referências apontam para objetos de conteúdo que representam cada item em um determinado canal.

Os elementos em um RSS feed têm a seguinte hierarquia e atributos.


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



A tabela a seguir lista os elementos de canal em um RSS feed e as \_ Propriedades de conversão de mídia do tipo de conteúdo WPD correspondente \_ \_ \_ .



| Elemento Channel | Requisito de RSS feed | Propriedade Mediacast correspondente      |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| category            | Opcional.                | [\_gênero de mídia WPD \_](media-properties.md)                       |
| nuvem               | Não aplicável.          | Não aplicável.                                                                 |
| direitos autorais           | Opcional.                | [\_ \_ direitos autorais de mídia WPD](media-properties.md)               |
| descrição         | Obrigatórios.                | [\_Descrição da mídia WPD \_](media-properties.md)           |
| docs                | Não aplicável.          | Não aplicável.                                                                 |
| gerador           | Não aplicável.          | Não aplicável.                                                                 |
| Linguagem            | Não aplicável.          | Não aplicável.                                                                 |
| lastBuildDate       | Opcional.                | [DATA DO \_ ÚLTIMO BUILD DA \_ MÍDIA \_ \_ WPD](media-properties.md) |
| link                | Obrigatórios.                | [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md)  |
| managingEditor      | Opcional.                | [EDITOR DE GERENCIAMENTO DE MÍDIA WPD \_ \_ \_](media-properties.md)  |
| pubDate             | Opcional.                | [WPD \_ MEDIA \_ RELEASE \_ DATE](media-properties.md)        |
| classificação              | Não aplicável.          | Não aplicável.                                                                 |
| skipDays            | Não aplicável.          | Não aplicável.                                                                 |
| skipHours           | Não aplicável.          | Não aplicável.                                                                 |
| Textinput           | Não aplicável.          | Não aplicável.                                                                 |
| title               | Obrigatórios.                | [NOME DO OBJETO WPD \_ \_](object-properties.md)                      |
| ttl                 | Opcional.                | [TEMPO DE \_ \_ VIDA DE MÍDIA \_ WPD \_](media-properties.md)       |
| Webmaster           | Opcional.                | [WPD \_ MEDIA \_ WEBMASTER](media-properties.md)               |



 

A tabela a seguir lista os elementos de imagem em um RSS feed e as propriedades CORRESPONDENTES WPD \_ CONTENT \_ TYPE MEDIA \_ \_ CAST.



| Elemento de imagem | Requisito do RSS Feed | Propriedade Mediacast                     |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| descrição       | Opcional.                | [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)          |
| altura            | Opcional.                | [ALTURA DA MÍDIA WPD \_ \_](media-properties.md)                    |
| link              | Opcional.                | [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md) |
| title             | Opcional.                | [NOME DO OBJETO WPD \_ \_](object-properties.md)                     |
| url               | Opcional.                | [\_URL de \_ origem de mídia WPD \_](media-properties.md)           |
| width             | Opcional.                | [\_largura de mídia WPD \_](media-properties.md)                      |



 

A tabela a seguir lista os elementos de item em um RSS feed e as \_ Propriedades de conversão de mídia do tipo de conteúdo WPD correspondente \_ \_ \_ .



| Elemento Item | Atributo | Requisito de RSS feed | Propriedade Mediacast  |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| autor           |               | Opcional.                | [\_artista de mídia WPD \_](media-properties.md)                    |
| category         |               | Opcional.                | [\_gênero de mídia WPD \_](media-properties.md)                      |
|                  | domínio        | Não aplicável.          | Não aplicável.                                                                |
| descrição      |               | Opcional.                | [\_Descrição da mídia WPD \_](media-properties.md)          |
| SPE        |               | Opcional.                |                                                                                |
|                  | url           | Obrigatórios.                | [\_URL de \_ origem de mídia WPD \_](media-properties.md)           |
|                  | comprimento        | Obrigatórios.                | [\_tamanho do objeto WPD \_](object-properties.md)                     |
|                  | tipo          | Obrigatórios.                | (O tipo MIME deve ser mapeado para o tipo de conteúdo da propriedade.)                 |
| guid             |               | Opcional.                | [\_GUID de mídia WPD \_](media-properties.md)                        |
|                  | IsLink permanente   | Não aplicável.          | Não aplicável.                                                                |
| link             |               | Opcional.                | [\_URL de \_ destino de mídia WPD \_](media-properties.md) |
| pubDate          |               | Opcional.                | [\_data de \_ lançamento de mídia WPD \_](media-properties.md)       |
| source           |               | Não aplicável.          | Não aplicável.                                                                |
| title            |               | Opcional.                | [\_nome do objeto WPD \_](object-properties.md)                     |



 

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
    <link>https://www.lucernepublishing.com/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past 5 years and their implications.</description>
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



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>Mapeando elementos de canal RSS para valores de propriedade WPD

A tabela a seguir descreve como os valores nos elementos do canal RSS no exemplo anterior são mapeados para propriedades WPD específicas.



| Propriedade WPD | Valor |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [DIREITOS \_ AUTORAIS DA MÍDIA WPD \_](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. Todos os direitos reservados.                                        |
| [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)                        | O CEO da Lucerne Publishing Peter Bankov dá uma olhada nas tendências mais recentes em publicações online. |
| [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [GÊNERO DE MÍDIA WPD \_ \_](media-properties.md)                                    | Notícias                                                                                          |
| [DATA DO \_ ÚLTIMO BUILD DA \_ MÍDIA \_ \_ WPD](media-properties.md)              | Sexta-feira, 9 de junho de 2006, 14:00:28 EDT                                                                 |
| [EDITOR DE GERENCIAMENTO DE MÍDIA WPD \_ \_ \_](media-properties.md)               | someone@example.com                                                                           |
| [WPD \_ MEDIA \_ RELEASE \_ DATE](media-properties.md)                     | Sexta-feira, 9 de junho de 2006, 14:00:28 EDT                                                                 |
| [TEMPO DE \_ \_ VIDA DE MÍDIA \_ WPD \_](media-properties.md)                    | 240                                                                                           |
| [TÍTULO DA \_ MÍDIA \_ WPD](media-properties.md)                                    | A publicação digital                                                                       |
| [URL DE \_ ORIGEM \_ DA MÍDIA WPD \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [WPD \_ MEDIA \_ WEBMASTER](media-properties.md)                            | someone@example.com                                                                           |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                  | CAST DE MÍDIA \_ DO \_ TIPO DE \_ CONTEÚDO \_ WPD                                                               |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                  | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [\_formato de objeto WPD \_](object-properties.md)                               | \_conversão de \_ \_ mídia abstrata \_ de formato de objeto WPD \_                                                    |
| [\_ID de objeto WPD \_](object-properties.md)                                       | Valor dependente da sessão.                                                                      |
| [\_nome do objeto WPD \_](object-properties.md)                                   | A publicação digital                                                                       |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)     | A publicação digital                                                                       |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                        | Mypodcasts (uma pasta de podcast fictícia no dispositivo). Suponha que "0A0" para este exemplo.        |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md) | Valor independente de sessão. (Suponha "0A1" para este exemplo.)                                   |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                       | 0A2 para N itens<br/>                                                                   |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                   | 13,790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Mapeando elementos de imagem RSS para valores de propriedade WPD

A tabela a seguir descreve como os valores nos elementos da Imagem RSS no exemplo anterior são mapeados para propriedades WPD específicas.



| Propriedade WPD               |                         Valor                                           |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)                                                   | Logotipo lucerne                                        |
| [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [ALTURA DA MÍDIA WPD \_ \_](media-properties.md)                                                             | 300                                                 |
| [URL DE \_ ORIGEM \_ DA MÍDIA WPD \_](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [LARGURA DE MÍDIA WPD \_ \_](media-properties.md)                                                               | 300                                                 |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                              | Lucerne Publishing                                  |
| [O ATRIBUTO \_ DE RECURSO \_ WPD PODE \_ \_ EXCLUIR](attributes.md)                               | VARIANT \_ TRUE                                       |
| [O ATRIBUTO DE RECURSO WPD \_ \_ PODE \_ \_ LER](attributes.md)                                   | VARIANT \_ TRUE                                       |
| [FORMATO DE \_ ATRIBUTO DE \_ RECURSO WPD \_](resource-attribute-properties.md)                     | \_GIF de \_ formato de objeto WPD \_                            |
| [\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_](attributes.md) | 1024                                                |
| [\_ \_ Tamanho total do atributo de recurso WPD \_ \_](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Mapeando elementos de item RSS para valores de propriedade WPD

A tabela a seguir descreve como os valores nos elementos de item RSS no exemplo anterior são mapeados para determinadas propriedades WPD.



| Propriedade WPD  | Valor                   |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [\_título de mídia WPD \_](media-properties.md)                                    | A publicação digital                                                                                                          |
| [\_duração da mídia WPD \_](media-properties.md)                              | 10329011                                                                                                                         |
| [\_artista de mídia WPD \_](media-properties.md)                                  | Zulu                                                                                                                          |
| [\_Descrição da mídia WPD \_](media-properties.md)                        | Publicações online estão mudando rapidamente. Um CEO da casa de publicação examina as tendências dos últimos 5 anos e suas implicações. |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_gênero de mídia WPD \_](media-properties.md)                                    | Notícias                                                                                                                             |
| [\_GUID de mídia WPD \_](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_data de \_ lançamento de mídia WPD \_](media-properties.md)                     | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                   |
| [URL DE \_ ORIGEM \_ DA MÍDIA WPD \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)            | 0A1                                                                                                                              |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                  | IMAGEM DE MÍDIA \_ DO \_ TIPO DE CONTEÚDO \_ WPD \_                                                                                                 |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                | June, 1 de junho de 2006 14:00:28 EDT                                                                                                   |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                  | June, 1 de junho de 2006 14:00:28 EDT                                                                                                   |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                | June, 1 de junho de 2006 14:00:28 EDT                                                                                                   |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                               | FORMATO DE OBJETO WPD \_ \_ \_ MP3                                                                                                         |
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                       | Dependente de sessão. (Suponha "0A2" para este exemplo.)                                                                              |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                   | A publicação digital                                                                                                          |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                        | 0A0                                                                                                                              |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md) | Independente de sessão.                                                                                                             |
| [\_tamanho do objeto WPD \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




