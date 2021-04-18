---
description: Apresenta o esquema de descrição do conector de pesquisa que é usado pelas bibliotecas do Windows Explorer e pelos provedores de Pesquisa Federados.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Esquema de descrição do conector de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789246"
---
# <a name="search-connector-description-schema"></a>Esquema de descrição do conector de pesquisa

Apresenta o esquema de descrição do conector de pesquisa que é usado pelas bibliotecas do Windows Explorer e pelos provedores de Pesquisa Federados. O esquema especifica a estrutura e os requisitos para os arquivos de descrição do conector de pesquisa ( \* . searchConnector-MS) e para os elementos **searchConnectorDescriptionType** dos arquivos de descrição da biblioteca do Shell ( \* . Library-MS).

Este tópico descreve o esquema conforme ele está relacionado aos conectores de Pesquisa Federados. Para obter mais informações sobre bibliotecas e o esquema de descrição da biblioteca, consulte o [esquema de descrição da biblioteca](../shell/library-schema-entry.md).

Este tópico inclui as seções a seguir:

-   [O que são conectores de pesquisa?](#what-are-search-connectors)
-   [Como os arquivos de descrição do conector de pesquisa funcionam?](#search-connector-description-schema)
-   [O que é o esquema de descrição do conector de pesquisa?](#what-is-the-search-connector-description-schema)
-   [Quais são as principais partes do esquema?](#what-are-the-major-parts-of-the-schema)
-   [Exemplos de arquivos de descrição do conector de pesquisa](#examples-of-search-connector-description-files)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="what-are-search-connectors"></a>O que são conectores de pesquisa?

Conectores de pesquisa conectam usuários com dados armazenados em serviços Web ou locais de armazenamento remoto. Com o Windows 7, os usuários podem instalar conectores de pesquisa para locais, como serviços Web, para que eles pesquisem esses locais diretamente do Windows Explorer. Os conectores de pesquisa são arquivos de descrição do conector de pesquisa ( \* . searchConnector-MS) que especificam como se conectar, enviar consultas e receber resultados do local.

Além dos serviços Web, os conectores de pesquisa podem ser usados para pesquisar escopos de índice locais criados por manipuladores de protocolo. Por exemplo, os usuários podem pesquisar emails indexados localmente com o manipulador de protocolo MAPI usando um conector de pesquisa para esse armazenamento de email.

## <a name="how-do-search-connector-description-files-work"></a>Como os arquivos de descrição do conector de pesquisa funcionam?

Quando os arquivos de descrição do conector de pesquisa são instalados nos sistemas dos usuários, os usuários podem abrir o Windows Explorer, clicar no conector de pesquisa no painel de navegação e inserir uma consulta de pesquisa. O Windows Explorer envia a consulta usando informações do arquivo de descrição do conector de pesquisa, como qual provedor usar e o escopo da pesquisa. Os resultados são retornados como itens RSS ou Atom feed e exibidos para os usuários como se fossem itens de shell regulares.

A maneira como você implanta o arquivo de descrição do conector de pesquisa depende do tipo de local ao qual o conector de pesquisa dá suporte:

-   Em um \* arquivo de configuração de OpenSearch (. osdx) para seu serviço Web
-   Como parte da instalação do manipulador de protocolo

Você deve garantir que os seguintes itens ocorram quando um usuário abrir o arquivo. osdx ou instalar o manipulador de protocolo:

-   O arquivo. searchconnector-MS é criado na pasta de **pesquisas do Windows** dos usuários (% USERPROFILE%/Searches).
-   Um atalho para o arquivo. searchconnector-MS é criado na pasta **links** dos usuários (% USERPROFILE%/links).

## <a name="what-is-the-search-connector-description-schema"></a>O que é o esquema de descrição do conector de pesquisa?

O esquema de descrição do conector de pesquisa é um esquema XML que define a estrutura dos arquivos de descrição do conector de pesquisa ( \* . searchConnector-MS). Cada conector de pesquisa deve ter um arquivo de descrição do conector de pesquisa que especifica como se conectar, enviar consultas e receber resultados do local.

## <a name="what-are-the-major-parts-of-the-schema"></a>Quais são as principais partes do esquema?

A tabela a seguir lista as partes principais do esquema.



| Elementos filho                                                                         | Description                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isSearchOnlyItem](search-schema-sconn-issearchonlyitem.md)                           | Identifica se os locais com suporte do conector de pesquisa são somente pesquisa ou pesquisa e procura.                                                                                |
| [isDefaultSaveLocation](search-schema-sconn-isdefaultsavelocation.md)                 | Somente para uso de biblioteca.                                                                                                                                                                   |
| [isDefaultNonOwnerSaveLocation](search-schema-sconn-isdefaultnonownersavelocation.md) | Somente para uso de biblioteca.                                                                                                                                                                   |
| [descrição](search-schema-sconn-description.md)                                     | Descreve o conector de pesquisa.                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | Identifica o local de um ícone personalizado para o conector de pesquisa.                                                                                                                      |
| [imageLink](search-schema-sconn-imagelink.md)                                         | Identifica o local de uma miniatura personalizada para o conector de pesquisa.                                                                                                                 |
| [autorização](search-schema-sconn-author.md)                                               | Identifica o autor do conector de pesquisa.                                                                                                                                          |
| [dateCreated](search-schema-sconn-datecreated.md)                                     | Identifica a data em que o conector de pesquisa foi criado.                                                                                                                              |
| [templateInfo](search-schema-sconn-templateinfo.md)                                   | Especifica um tipo de pasta para o conector de pesquisa.                                                                                                                                       |
| [LocalProvider](search-schema-sconn-locationprovider.md)                           | Especifica o provedor de pesquisa a ser usado por este conector de pesquisa.                                                                                                                      |
| [escopo](search-schema-sconn-scope.md)                                                 | Especifica os locais a serem incluídos e excluídos do escopo de pesquisa.                                                                                                                |
| [propertyStore](search-schema-sconn-propertystore.md)                                 | Especifica o local de um [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) baseado em XML para esse conector de pesquisa. O **IPropertyStore** dá suporte aos metadados abertos do conector de pesquisa. |
| [includeInStartMenuScope](search-schema-sconn-includeinstartmenuscope.md)             | Especifica se o local representado pelo conector de pesquisa deve ser incluído no escopo de pesquisa do menu iniciar.                                                                 |
| [controlador](search-schema-sconn-domain.md)                                               | Identifica o domínio de nível superior do conector de pesquisa.                                                                                                                                     |
| [supportsAdvancedQuerySyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | Especifica se o conector de pesquisa dá suporte à sintaxe de consulta avançada (AQS).                                                                                                            |
| [IsIndexed](search-schema-sconn-isindexed.md)                                         | Especifica se o local representado pelo conector de pesquisa é indexado.                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>Exemplos de arquivos de descrição do conector de pesquisa

Veja a seguir um exemplo de um arquivo de descrição do conector de pesquisa para um serviço Web de pesquisa federado.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



Veja a seguir um exemplo de um arquivo de descrição do conector de pesquisa para um manipulador de protocolo MAPI.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a>Recursos adicionais

-   Para obter mais informações sobre o esquema de descrição da biblioteca, consulte o [esquema de descrição da biblioteca](../shell/library-schema-entry.md).
-   Para obter mais informações sobre como instalar um conector de pesquisa, consulte [pesquisa federada no Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[OpenSearch](http://www.opensearch.org/Home)
</dt> <dt>

[Centro de Download da Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
