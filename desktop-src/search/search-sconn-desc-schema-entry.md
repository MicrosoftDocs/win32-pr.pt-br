---
description: Apresenta o esquema de Descrição do Conector de Pesquisa usado por bibliotecas Windows Explorer e provedores de pesquisa federados.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Esquema de descrição do conector de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8d8ab60ba472cca961a4208b1c551679ef93eacd46e07cf5e080a3e73f3d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226377"
---
# <a name="search-connector-description-schema"></a>Esquema de descrição do conector de pesquisa

Apresenta o esquema de Descrição do Conector de Pesquisa usado por bibliotecas Windows Explorer e provedores de pesquisa federados. O esquema especifica a estrutura e os requisitos para arquivos de Descrição do Conector de Pesquisa ( \* .searchConnector-ms) e para elementos **searchConnectorDescriptionType** dos arquivos de Descrição da Biblioteca do Shell ( \* .library-ms).

Este tópico descreve o esquema relacionado aos conectores de pesquisa federados. Para obter mais informações sobre bibliotecas e o esquema de Descrição da Biblioteca, consulte [Esquema de Descrição da Biblioteca](../shell/library-schema-entry.md).

Este tópico inclui as seções a seguir:

-   [O que são conectores de pesquisa?](#what-are-search-connectors)
-   [Como funcionam os arquivos de descrição do conector de pesquisa?](#search-connector-description-schema)
-   [O que é o esquema de descrição do conector de pesquisa?](#what-is-the-search-connector-description-schema)
-   [Quais são as principais partes do esquema?](#what-are-the-major-parts-of-the-schema)
-   [Exemplos de arquivos de descrição do conector de pesquisa](#examples-of-search-connector-description-files)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="what-are-search-connectors"></a>O que são conectores de pesquisa?

Os conectores de pesquisa conectam os usuários aos dados armazenados em serviços Web ou locais de armazenamento remoto. Com Windows 7, os usuários podem instalar conectores de pesquisa para locais, como serviços Web, para que eles pesquisem esses locais diretamente do Windows Explorer. Os conectores de pesquisa são arquivos de Descrição do Conector de Pesquisa ( .searchConnector-ms) que especificam como se conectar, enviar consultas e receber resultados \* do local.

Além dos serviços Web, os conectores de pesquisa podem ser usados para pesquisar escopos de índice local criados por manipuladores de protocolo. Por exemplo, os usuários podem pesquisar email indexado localmente com o manipulador de protocolo MAPI usando um conector de pesquisa para esse armazenamento de email.

## <a name="how-do-search-connector-description-files-work"></a>Como funcionam os arquivos de descrição do conector de pesquisa?

Quando os arquivos de Descrição do Conector de Pesquisa são instalados nos sistemas dos usuários, os usuários podem abrir o Windows Explorer, clicar no conector de pesquisa no painel de navegação e inserir uma consulta de pesquisa. Windows O Explorer envia a consulta usando informações do arquivo Descrição do Conector de Pesquisa, como qual provedor usar e o escopo da pesquisa. Os resultados são retornados como itens de feed RSS ou Atom e exibidos aos usuários como se fossem itens de Shell regulares.

A maneira como você implanta o arquivo Descrição do Conector de Pesquisa depende do tipo de local ao qual o conector de pesquisa dá suporte:

-   Em um arquivo OpenSearch \* (.osdx) para seu serviço Web
-   Como parte da instalação do manipulador de protocolo

Você deve garantir que as seguintes coisas aconteçam quando um usuário abrir o arquivo .osdx ou instalar o manipulador de protocolo:

-   O arquivo .searchconnector-ms é criado na pasta **Windows Searches** dos usuários (%userprofile%/Searches).
-   Um atalho para o arquivo .searchconnector-ms é criado na pasta **Links** dos usuários (%userprofile%/Links).

## <a name="what-is-the-search-connector-description-schema"></a>O que é o esquema de descrição do conector de pesquisa?

O esquema Descrição do Conector de Pesquisa é um esquema XML que define a estrutura dos arquivos de Descrição do Conector de Pesquisa ( \* .searchConnector-ms). Cada conector de pesquisa deve ter um arquivo de Descrição do Conector de Pesquisa que especifica como se conectar, enviar consultas e receber resultados do local.

## <a name="what-are-the-major-parts-of-the-schema"></a>Quais são as principais partes do esquema?

A tabela a seguir lista as principais partes do esquema.



| Elementos filho                                                                         | Descrição                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isSearchOnlyItem](search-schema-sconn-issearchonlyitem.md)                           | Identifica se os locais com suporte pelo conector de pesquisa são somente pesquisa ou pesquisa e procura.                                                                                |
| [isDefaultSaveLocation](search-schema-sconn-isdefaultsavelocation.md)                 | Somente para uso de biblioteca.                                                                                                                                                                   |
| [isDefaultNonOwnerSaveLocation](search-schema-sconn-isdefaultnonownersavelocation.md) | Somente para uso de biblioteca.                                                                                                                                                                   |
| [descrição](search-schema-sconn-description.md)                                     | Descreve o conector de pesquisa.                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | Identifica o local de um ícone personalizado para o conector de pesquisa.                                                                                                                      |
| [imageLink](search-schema-sconn-imagelink.md)                                         | Identifica o local de uma miniatura personalizada para o conector de pesquisa.                                                                                                                 |
| [Autor](search-schema-sconn-author.md)                                               | Identifica o autor do conector de pesquisa.                                                                                                                                          |
| [Datecreated](search-schema-sconn-datecreated.md)                                     | Identifica a data em que o conector de pesquisa foi criado.                                                                                                                              |
| [Templateinfo](search-schema-sconn-templateinfo.md)                                   | Especifica um tipo de pasta para o conector de pesquisa.                                                                                                                                       |
| [locationProvider](search-schema-sconn-locationprovider.md)                           | Especifica o provedor de pesquisa a ser usado por esse conector de pesquisa.                                                                                                                      |
| [escopo](search-schema-sconn-scope.md)                                                 | Especifica os locais a incluir e excluir do escopo de pesquisa.                                                                                                                |
| [Propertystore](search-schema-sconn-propertystore.md)                                 | Especifica o local de um [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) baseado em XML para esse conector de pesquisa. O **IPropertyStore dá** suporte aos metadados abertos do conector de pesquisa. |
| [includeInStartMenuScope](search-schema-sconn-includeinstartmenuscope.md)             | Especifica se o local representado pelo conector de pesquisa deve ser incluído no escopo menu Iniciar pesquisa do usuário.                                                                 |
| [Domínio](search-schema-sconn-domain.md)                                               | Identifica o domínio de nível superior do conector de pesquisa.                                                                                                                                     |
| [supportsAdvancedQuerySyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | Especifica se o conector de pesquisa dá suporte à AQS (Advanced Query Syntax).                                                                                                            |
| [isIndexed](search-schema-sconn-isindexed.md)                                         | Especifica se o local representado pelo conector de pesquisa é indexado.                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>Exemplos de arquivos de descrição do conector de pesquisa

A seguir está um exemplo de um arquivo de Descrição do Conector de Pesquisa para um serviço Web de pesquisa federada.


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



A seguir está um exemplo de um arquivo de Descrição do Conector de Pesquisa para um manipulador de protocolo MAPI.


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

-   Para obter mais informações sobre o esquema de Descrição da Biblioteca, consulte [Esquema de Descrição da Biblioteca](../shell/library-schema-entry.md).
-   Para obter mais informações sobre como instalar um conector de pesquisa, [consulte Pesquisa federada no Windows](-search-federated-search-overview.md).

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

 

 
