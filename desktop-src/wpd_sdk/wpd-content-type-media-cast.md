---
description: CAST DE MÍDIA \_ DO \_ TIPO DE \_ CONTEÚDO \_ WPD
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4454053400c783b53437dd025e5adc8e845ea08c1b95b8d9b1fd358f39e326f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083310"
---
# <a name="wpd_content_type_media_cast"></a>CAST DE MÍDIA \_ DO \_ TIPO DE \_ CONTEÚDO \_ WPD

Um objeto que descreve seu tipo como WPD \_ CONTENT TYPE MEDIA CAST representa uma coleção de conteúdo \_ \_ \_ relacionado.

Um objeto Mediacast pode ser pensado como um objeto de contêiner que grupos de conteúdo relacionado, assim como uma música de grupos de playlists. Geralmente, um objeto Mediacast é usado para agrupar o conteúdo de mídia que foi publicado online. Por exemplo, um canal RSS pode ser representado como um objeto Mediacast cujas referências de objeto apontam para objetos de conteúdo que representam cada item no canal.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade             |  Obrigatório ou Opcional         |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                | Obrigatórios.                                                             |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                 | Obrigatórios.                                                             |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                             |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                          | Obrigatórios.                                                             |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                        | Obrigatórios.                                                             |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                           | Obrigatórios.                                                             |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                     |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                    | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema). |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                     |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                              | Necessário se o objeto representar um arquivo.                             |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                       | Recomendado se o objeto não for destinado ao consumo pelo dispositivo. |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                | Necessário se o objeto tiver referências a outros objetos.               |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                    | Opcional.                                                             |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                     | Opcional.                                                             |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                           | Opcional.                                                             |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                         | Recomendável.                                                          |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                         | Opcional.                                                             |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                     | Recomendado se o objeto for referenciado por outro objeto.            |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                             |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md) | Opcional.                                                             |
| [O OBJETO WPD \_ \_ PODE \_ EXCLUIR](object-properties.md)                                               | Necessário se o objeto puder ser excluído.                                |
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
| [INDICADOR DE \_ OBJETO \_ DE MÍDIA \_ WPD](media-properties.md)                                        | Recomendado                                                           |
| [DATA DO \_ ÚLTIMO BUILD DA \_ MÍDIA \_ \_ WPD](media-properties.md)                                       | Recomendável.                                                          |
| [TEMPO DE \_ \_ VIDA DE MÍDIA \_ WPD \_](media-properties.md)                                             | Opcional.                                                             |
| [SUB DESCRIÇÃO DA MÍDIA WPD \_ \_ \_](object-properties.md)                                                                 | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os recursos a seguir.



| Nome do Recurso                                               | Obrigatório ou Opcional | Descrição                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)      | Opcional.            | Contém os dados do arquivo mediacast. Por exemplo, se este mediacast representar um canal RSS, esse poderá ser o documento RSS. |
| [**MINIATURA DO RECURSO WPD \_ \_**](wpd-resource-thumbnail.md)  | Opcional.            | Contém a miniatura que representa este mediacast.                                                                         |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md) | Opcional.            | Contém a arte deste mediacast.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Mapeamento de elementos RSS e propriedades mediacast

Um canal RSS pode ser representado como um objeto Mediacast cujas referências apontam para objetos de conteúdo que representam cada item em um determinado canal.

Os elementos em um RSS feed têm a hierarquia e os atributos a seguir.


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



A tabela a seguir lista os elementos de canal em um RSS feed e as propriedades CORRESPONDENTES WPD \_ CONTENT \_ TYPE MEDIA \_ \_ CAST.



| Elemento Channel | Requisito do RSS Feed | Propriedade Mediacast correspondente      |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| category            | Opcional.                | [GÊNERO DE MÍDIA WPD \_ \_](media-properties.md)                       |
| nuvem               | Não aplicável.          | Não aplicável.                                                                 |
| direitos autorais           | Opcional.                | [DIREITOS \_ AUTORAIS DA MÍDIA WPD \_](media-properties.md)               |
| descrição         | Obrigatórios.                | [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)           |
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
| título               | Obrigatórios.                | [NOME DO OBJETO WPD \_ \_](object-properties.md)                      |
| ttl                 | Opcional.                | [TEMPO DE \_ \_ VIDA DE MÍDIA \_ WPD \_](media-properties.md)       |
| Webmaster           | Opcional.                | [WPD \_ MEDIA \_ WEBMASTER](media-properties.md)               |



 

A tabela a seguir lista os elementos de imagem em um RSS feed e as propriedades WPD \_ CONTENT TYPE MEDIA CAST \_ \_ \_ correspondentes.



| Elemento de imagem | Requisito do RSS Feed | Propriedade Mediacast                     |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| descrição       | Opcional.                | [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)          |
| altura            | Opcional.                | [ALTURA DA MÍDIA WPD \_ \_](media-properties.md)                    |
| link              | Opcional.                | [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md) |
| título             | Opcional.                | [NOME DO OBJETO WPD \_ \_](object-properties.md)                     |
| url               | Opcional.                | [URL DE \_ ORIGEM \_ DA MÍDIA WPD \_](media-properties.md)           |
| width             | Opcional.                | [LARGURA DE MÍDIA WPD \_ \_](media-properties.md)                      |



 

A tabela a seguir lista os elementos de item em um RSS feed e as propriedades CORRESPONDENTES WPD \_ CONTENT \_ TYPE MEDIA \_ \_ CAST.



| Elemento Item | Atributo | Requisito do RSS Feed | Propriedade Mediacast  |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| autor           |               | Opcional.                | [WPD \_ MEDIA \_ ARTIST](media-properties.md)                    |
| category         |               | Opcional.                | [GÊNERO DE MÍDIA WPD \_ \_](media-properties.md)                      |
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



| Propriedade WPD | Valor |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [\_ \_ direitos autorais de mídia WPD](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. Todos os direitos reservados.                                        |
| [\_Descrição da mídia WPD \_](media-properties.md)                        | A Lucerne Publishing CEO Peter Bankov analisa as tendências mais recentes em publicações online. |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [\_gênero de mídia WPD \_](media-properties.md)                                    | News                                                                                          |
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



| Propriedade WPD               |                         Valor                                           |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [\_Descrição da mídia WPD \_](media-properties.md)                                                   | Logotipo da Lucerne                                        |
| [\_URL de \_ destino de mídia WPD \_](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [\_altura de mídia WPD \_](media-properties.md)                                                             | 300                                                 |
| [\_URL de \_ origem de mídia WPD \_](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [\_largura de mídia WPD \_](media-properties.md)                                                               | 300                                                 |
| [\_nome do objeto WPD \_](object-properties.md)                                                              | Publicação na editora                                  |
| [o \_ atributo de recurso WPD \_ \_ pode \_ excluir](attributes.md)                               | VARIANTE \_ true                                       |
| [O ATRIBUTO DE RECURSO WPD \_ \_ PODE \_ \_ LER](attributes.md)                                   | VARIANT \_ TRUE                                       |
| [FORMATO DE \_ ATRIBUTO DE \_ RECURSO WPD \_](resource-attribute-properties.md)                     | GIF DE FORMATO \_ DE \_ OBJETO \_ WPD                            |
| [TAMANHO IDEAL DO BUFFER DE \_ \_ LEITURA DO ATRIBUTO \_ \_ \_ \_ DE RECURSO WPD](attributes.md) | 1024                                                |
| [TAMANHO TOTAL \_ DO \_ ATRIBUTO DE RECURSO \_ WPD \_](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Mapeando elementos de item RSS para valores de propriedade WPD

A tabela a seguir descreve como os valores nos elementos do Item RSS no exemplo anterior são mapeados para propriedades WPD específicas.



| Propriedade WPD  | Valor                   |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [TÍTULO DA \_ MÍDIA \_ WPD](media-properties.md)                                    | A publicação digital                                                                                                          |
| [DURAÇÃO DA \_ MÍDIA \_ WPD](media-properties.md)                              | 10329011                                                                                                                         |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                  | Lucerna                                                                                                                          |
| [DESCRIÇÃO DA MÍDIA WPD \_ \_](media-properties.md)                        | As publicações online estão mudando rapidamente. Um CEO da casa de publicação examina as tendências dos últimos 5 anos e suas implicações. |
| [URL DE DESTINO DE MÍDIA WPD \_ \_ \_](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [GÊNERO DE MÍDIA WPD \_ \_](media-properties.md)                                    | News                                                                                                                             |
| [GUID DE \_ MÍDIA WPD \_](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [WPD \_ MEDIA \_ RELEASE \_ DATE](media-properties.md)                     | Ela, 1º de junho de 2006, 14:00:28 EDT                                                                                                   |
| [URL DE \_ ORIGEM \_ DA MÍDIA WPD \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)            | 0A1                                                                                                                              |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                  | IMAGEM DE MÍDIA \_ DO \_ TIPO DE \_ CONTEÚDO \_ WPD                                                                                                 |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                | Ela, 1º de junho de 2006, 14:00:28 EDT                                                                                                   |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                  | Ela, 1º de junho de 2006, 14:00:28 EDT                                                                                                   |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                | Ela, 1º de junho de 2006, 14:00:28 EDT                                                                                                   |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                               | FORMATO DE OBJETO WPD \_ \_ \_ MP3                                                                                                         |
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                       | Dependente de sessão. (Suponha "0A2" para este exemplo.)                                                                              |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                   | A publicação digital                                                                                                          |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                        | 0A0                                                                                                                              |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md) | Independente de sessão.                                                                                                             |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




