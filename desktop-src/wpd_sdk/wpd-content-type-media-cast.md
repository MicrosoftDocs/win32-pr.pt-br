---
description: '\_conversão de \_ mídia de tipo de conteúdo WPD \_ \_'
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2daafb381aac802b9add130aa97e9750f30e7847
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091897"
---
# <a name="wpd_content_type_media_cast"></a>\_conversão de \_ mídia de tipo de conteúdo WPD \_ \_

Um objeto que descreve seu tipo de tipo de conteúdo WPD com \_ \_ \_ \_ conversão de mídia representa uma coleção de conteúdo relacionado.

Um objeto Mediacast pode ser considerado como um objeto de contêiner que agrupa conteúdo relacionado, assim como uma lista de reprodução de músicas. Geralmente, um objeto Mediacast é usado para agrupar o conteúdo de mídia que foi publicado online. Por exemplo, um canal RSS pode ser representado como um objeto Mediacast, cujas referências de objeto apontam para objetos de conteúdo que representam cada item no canal.

Esse tipo de objeto dá suporte às propriedades a seguir.



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Nome da propriedade**                                                                                                     | **Obrigatório ou opcional**                                              |
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatórios.                                                             |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                             |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                             |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatórios.                                                             |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                             |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                             |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                     |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema). |
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
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Obrigatório se o objeto não puder ser excluído.                             |
| [\_ \_ direitos autorais de mídia WPD](media-properties.md)                                                     | Opcional.                                                             |
| [\_classificação de \_ controle de nível de mídia WPD \_](media-properties.md)                                        | Opcional.                                                             |
| [metagênero de \_ mídia WPD \_ \_](media-properties.md)                                                  | Opcional.                                                             |
| [subtítulo de \_ mídia WPD \_ \_](media-properties.md)                                                    | Opcional.                                                             |
| [\_data de \_ lançamento de mídia WPD \_](media-properties.md)                                              | Recomendável.                                                          |
| [\_título de mídia WPD \_](media-properties.md)                                                             | Recomendável.                                                          |
| [\_proprietário da mídia WPD \_](media-properties.md)                                                             | Recomendável.                                                          |
| [\_Editor de \_ Gerenciamento de mídia WPD \_](media-properties.md)                                        | Recomendável.                                                          |
| [\_webmaster de mídia WPD \_](media-properties.md)                                                     | Recomendável.                                                          |
| [\_URL de \_ origem de mídia WPD \_](media-properties.md)                                                  | Recomendável.                                                          |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)                                        | Recomendável.                                                          |
| [\_Descrição da mídia WPD \_](media-properties.md)                                                 | Opcional.                                                             |
| [\_gênero de mídia WPD \_](media-properties.md)                                                             | Opcional.                                                             |
| [\_indicador de \_ objeto de mídia WPD \_](media-properties.md)                                        | Recomendadas                                                           |
| [\_data da \_ última \_ compilação da mídia \_ WPD](media-properties.md)                                       | Recomendável.                                                          |
| [\_vida útil \_ \_ de mídia \_ WPD](media-properties.md)                                             | Opcional.                                                             |
| [subdescrição de \_ mídia WPD \_ \_](object-properties.md)                                                                 | Opcional.                                                             |



 

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



|                     |                          |                                                                                 |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| **Elemento Channel** | **Requisito de RSS feed** | **Propriedade Mediacast correspondente**                                            |
| category            | Opcional.                | [\_gênero de mídia WPD \_](media-properties.md)                       |
| nuvem               | Não aplicável.          | Não aplicável.                                                                 |
| direitos autorais           | Opcional.                | [\_ \_ direitos autorais de mídia WPD](media-properties.md)               |
| descrição         | Obrigatórios.                | [\_Descrição da mídia WPD \_](media-properties.md)           |
| docs                | Não aplicável.          | Não aplicável.                                                                 |
| gerador           | Não aplicável.          | Não aplicável.                                                                 |
| Linguagem            | Não aplicável.          | Não aplicável.                                                                 |
| lastBuildDate       | Opcional.                | [\_data da \_ última \_ compilação da mídia \_ WPD](media-properties.md) |
| link                | Obrigatórios.                | [\_URL de \_ destino de mídia WPD \_](media-properties.md)  |
| managingEditor      | Opcional.                | [\_Editor de \_ Gerenciamento de mídia WPD \_](media-properties.md)  |
| pubDate             | Opcional.                | [\_data de \_ lançamento de mídia WPD \_](media-properties.md)        |
| classificação              | Não aplicável.          | Não aplicável.                                                                 |
| skipDays            | Não aplicável.          | Não aplicável.                                                                 |
| skipHours           | Não aplicável.          | Não aplicável.                                                                 |
| textInput           | Não aplicável.          | Não aplicável.                                                                 |
| título               | Obrigatórios.                | [\_nome do objeto WPD \_](object-properties.md)                      |
| ttl                 | Opcional.                | [\_vida útil \_ \_ de mídia \_ WPD](media-properties.md)       |
| webMaster           | Opcional.                | [\_webmaster de mídia WPD \_](media-properties.md)               |



 

A tabela a seguir lista os elementos de imagem em um RSS feed e as \_ Propriedades de conversão de mídia do tipo de conteúdo WPD correspondente \_ \_ \_ .



|                   |                          |                                                                                |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| **Elemento de imagem** | **Requisito de RSS feed** | **Propriedade Mediacast**                                                         |
| descrição       | Opcional.                | [\_Descrição da mídia WPD \_](media-properties.md)          |
| altura            | Opcional.                | [\_altura de mídia WPD \_](media-properties.md)                    |
| link              | Opcional.                | [\_URL de \_ destino de mídia WPD \_](media-properties.md) |
| título             | Opcional.                | [\_nome do objeto WPD \_](object-properties.md)                     |
| url               | Opcional.                | [\_URL de \_ origem de mídia WPD \_](media-properties.md)           |
| width             | Opcional.                | [\_largura de mídia WPD \_](media-properties.md)                      |



 

A tabela a seguir lista os elementos de item em um RSS feed e as \_ Propriedades de conversão de mídia do tipo de conteúdo WPD correspondente \_ \_ \_ .



|                  |               |                          |                                                                                |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| **Elemento item** | **Atributo** | **Requisito de RSS feed** | **Propriedade Mediacast**                                                         |
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
| título            |               | Opcional.                | [\_nome do objeto WPD \_](object-properties.md)                     |



 

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

A tabela a seguir descreve como os valores nos elementos do canal RSS no exemplo anterior são mapeados para determinadas propriedades WPD.



|                                                                                              |                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **Propriedade WPD**                                                                             | **Valor**                                                                                     |
| [\_ \_ direitos autorais de mídia WPD](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. Todos os direitos reservados.                                        |
| [\_Descrição da mídia WPD \_](media-properties.md)                        | A Lucerne Publishing CEO Peter Bankov analisa as tendências mais recentes em publicações online. |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [\_gênero de mídia WPD \_](media-properties.md)                                    | Notícias                                                                                          |
| [\_data da \_ última \_ compilação da mídia \_ WPD](media-properties.md)              | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [\_Editor de \_ Gerenciamento de mídia WPD \_](media-properties.md)               | someone@example.com                                                                           |
| [\_data de \_ lançamento de mídia WPD \_](media-properties.md)                     | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [\_vida útil \_ \_ de mídia \_ WPD](media-properties.md)                    | 240                                                                                           |
| [\_título de mídia WPD \_](media-properties.md)                                    | A publicação digital                                                                       |
| [\_URL de \_ origem de mídia WPD \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [\_webmaster de mídia WPD \_](media-properties.md)                            | someone@example.com                                                                           |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                  | \_conversão de \_ mídia de tipo de conteúdo WPD \_ \_                                                               |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                  | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                | Sexta-feira, 9 de junho de 2006 14:00:28 EDT                                                                 |
| [\_formato de objeto WPD \_](object-properties.md)                               | \_conversão de \_ \_ mídia abstrata \_ de formato de objeto WPD \_                                                    |
| [\_ID de objeto WPD \_](object-properties.md)                                       | Valor dependente da sessão.                                                                      |
| [\_nome do objeto WPD \_](object-properties.md)                                   | A publicação digital                                                                       |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)     | A publicação digital                                                                       |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                        | Mypodcasts (uma pasta de podcast fictícia no dispositivo). Suponha que "0A0" para este exemplo.        |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md) | Valor independente de sessão. (Suponha "0A1" para este exemplo.)                                   |
| [\_referências de objetos WPD \_](object-properties.md)                       | 0A2 para N itens<br/>                                                                   |
| [\_tamanho do objeto WPD \_](object-properties.md)                                   | 13.790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Mapeando elementos de imagem RSS para valores de propriedade WPD

A tabela a seguir descreve como os valores nos elementos da imagem RSS no exemplo anterior são mapeados para determinadas propriedades WPD.



|                                                                                                                         |                                                     |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Propriedade WPD**                                                                                                        | **Valor**                                           |
| [\_Descrição da mídia WPD \_](media-properties.md)                                                   | Logotipo da Lucerne                                        |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [\_altura de mídia WPD \_](media-properties.md)                                                             | 300                                                 |
| [\_URL de \_ origem de mídia WPD \_](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [\_largura de mídia WPD \_](media-properties.md)                                                               | 300                                                 |
| [\_nome do objeto WPD \_](object-properties.md)                                                              | Publicação na editora                                  |
| [o \_ atributo de recurso WPD \_ \_ pode \_ excluir](attributes.md)                               | VARIANTE \_ true                                       |
| [o \_ atributo de recurso WPD \_ \_ pode \_ ler](attributes.md)                                   | VARIANTE \_ true                                       |
| [\_formato de \_ atributo de recurso WPD \_](resource-attribute-properties.md)                     | \_GIF de \_ formato de objeto WPD \_                            |
| [\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_](attributes.md) | 1024                                                |
| [\_ \_ Tamanho total do atributo de recurso WPD \_ \_](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Mapeando elementos de item RSS para valores de propriedade WPD

A tabela a seguir descreve como os valores nos elementos de item RSS no exemplo anterior são mapeados para determinadas propriedades WPD.



|                                                                                              |                                                                                                                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **Propriedade WPD**<br/>                                                                  | **Valor**                                                                                                                        |
| [\_título de mídia WPD \_](media-properties.md)                                    | A publicação digital                                                                                                          |
| [\_duração da mídia WPD \_](media-properties.md)                              | 10329011                                                                                                                         |
| [\_artista de mídia WPD \_](media-properties.md)                                  | Zulu                                                                                                                          |
| [\_Descrição da mídia WPD \_](media-properties.md)                        | Publicações online estão mudando rapidamente. Um CEO da casa de publicação examina as tendências dos últimos 5 anos e suas implicações. |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_gênero de mídia WPD \_](media-properties.md)                                    | Notícias                                                                                                                             |
| [\_GUID de mídia WPD \_](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_data de \_ lançamento de mídia WPD \_](media-properties.md)                     | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                   |
| [\_URL de \_ origem de mídia WPD \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)            | 0A1                                                                                                                              |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                  | \_imagem de \_ mídia do tipo de conteúdo WPD \_ \_                                                                                                 |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                   |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                  | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                   |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                | Qui., 1 de junho de 2006 14:00:28 EDT                                                                                                   |
| [\_formato de objeto WPD \_](object-properties.md)                               | \_Formato de objeto WPD \_ \_ mp3                                                                                                         |
| [\_ID de objeto WPD \_](object-properties.md)                                       | Dependente da sessão. (Suponha "0A2" para este exemplo.)                                                                              |
| [\_nome do objeto WPD \_](object-properties.md)                                   | A publicação digital                                                                                                          |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                        | 0A0                                                                                                                              |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md) | Independente de sessão.                                                                                                             |
| [\_tamanho do objeto WPD \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




