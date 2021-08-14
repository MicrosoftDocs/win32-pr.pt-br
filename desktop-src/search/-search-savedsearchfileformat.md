---
description: Windows os usuários podem salvar pesquisas como uma Pasta de Pesquisa gerada por um arquivo XML que armazena a consulta em um formulário que pode ser usado pelo subsistema Windows search.
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: Formato de arquivo de pesquisa salvo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 614eb357a82d2c70e068a9fa5258974423d755c48e779d5f5fe8be184a864d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863719"
---
# <a name="saved-search-file-format"></a>Formato de arquivo de pesquisa salvo

No Windows Vista e posterior, os usuários podem salvar pesquisas como uma Pasta de Pesquisa que é gerada por um arquivo XML que armazena a consulta em um formulário que pode ser usado pelo subsistema Windows search. Este tópico descreve o formato de arquivo ( \* .search-ms) e inclui as seguintes seções:

- [Visão geral das pesquisas salvas](#overview-of-saved-searches)
- [\<viewInfo> Elemento](/windows)
  - [\<viewInfo> Atributos](/windows)
  - [\<viewInfo> Elementos filho](/windows)
- [\<query> Elemento](/windows)
  - [\<query> Elementos filho](/windows)
- [\<properties> Elemento](/windows)
- [Especificação completa do formato de arquivo search-ms](#full-specification-of-the-search-ms-file-format)
- [Exemplos de pesquisas salvas](#examples-of-saved-searches)

## <a name="overview-of-saved-searches"></a>Visão geral das pesquisas salvas

Os usuários podem salvar uma consulta de pesquisa como uma Pasta de Pesquisa, uma pasta virtual exibida Windows Explorer na pasta Pesquisas. Abrir uma Pasta de Pesquisa executa a pesquisa salva e exibe os resultados atualizados. O arquivo de pesquisa salvo armazena a consulta em um formato Windows Search pode agir, especificando o que pesquisar, onde pesquisar e como apresentar os resultados.

A pesquisa salva é gerada de um arquivo XML ( \* .search-ms) na pasta %userprofile% \\ Searches. Os dados são divididos em três elementos primários no arquivo XML:

- \<viewInfo> especifica informações de apresentação
- \<query> especifica (informações de consulta de pesquisa
- \<properties> especifica as propriedades do próprio \* arquivo .search-ms

O exemplo a seguir mostra a estrutura de alto nível de um arquivo de pesquisa salvo.

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">

    <viewInfo ...>
        ...
    </viewInfo>

    <query>
        ...
    </query>

    <properties>
        ...
    </properties>

</persistedQuery>
```

## <a name="viewinfo-element"></a>Elemento \<viewInfo>

O \<viewInfo> elemento especifica como os resultados são apresentados ao usuário final. O exemplo a seguir mostra a estrutura do elemento .

```XML
...
    <viewInfo viewMode=""
              iconSize=""
              stackIconSize=""
              autoListFlags=""
              folderFlags=""
              taskFlags=""
              displayName="">

        <visibleColumns>
            <column viewField=""/>
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/>
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>
        </columnChooserColumns >

        <groupBy viewField=""
                 direction=""/>

        <stackList>
            <stack viewField=""/>
        </stackList>

        <sortList>
            <sort viewField=""
                  direction=""/>
        </sortList>
    </viewInfo>
...
```

### <a name="viewinfo-attributes"></a>\<viewInfo> Atributos

A tabela a seguir descreve os atributos do elemento \<viewInfo>.

| Atributo     | Descrição                                                                     | Valores                     |
|---------------|---------------------------------------------------------------------------------|----------------------------|
| Viewmode      | Especifica a exibição de pasta.                                                      | Blocos \| de ícones \| de detalhes  |
| iconSize      | Controla o tamanho padrão dos ícones e miniaturas dos itens quando não são empilhados. | Inteiro entre 16 e 256 |
| stackIconSize | Somente para uso interno. Não use.                                              | n/d                        |
| displayName   | Somente para uso interno. Não use.                                              | n/d                        |
| autoListFlags | Somente para uso interno. Não use.                                              | n/d                        |
| folderFlags   | Somente para uso interno. Não use.                                              | n/d                        |
| taskFlags     | Somente para uso interno. Não use.                                              | n/d                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> Elementos filho

Os elementos filho do elemento especificam quais colunas aparecem nos resultados da pesquisa Windows Explorer e como os resultados são \<viewInfo> agrupados e classificação. Cada elemento filho contém um conjunto ordenado de colunas, identificado por nomes canônicos de propriedades do sistema (por exemplo, System.DisplayName). Se não estiver definido no arquivo de pesquisa salvo, os resultados da pesquisa serão apresentados com um conjunto padrão de colunas apropriado para os tipos de arquivo exibidos.

| Elemento               | Descrição                                                                                        | Valores                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| visibleColumns        | Especifica uma lista ordenada de colunas a aparecer na exibição de resultados. O usuário pode alterar essa lista. | Qualquer propriedade do sistema.                                         |
| frequentlyUsedColumns | Somente para uso interno. Não use.                                                                 | n/d                                                          |
| columnChooserColumns  | Somente para uso interno. Não use.                                                                 | n/d                                                          |
| Groupby               | Especifica uma única propriedade do sistema pela qual agrupar os resultados. O usuário pode alterar esse valor.  | Qualquer propriedade do sistema.                                         |
| Sortlist              | Especifica uma lista ordenada de colunas para classificar os resultados.                                       | Até quatro propriedades do sistema. O usuário pode alterar essa lista. |
| stackList             | Somente para uso interno. Não use.                                                                 | n/d                                                          |

## <a name="query-element"></a>Elemento \<query>

O \<query> elemento especifica os atributos que definem como os resultados são consultados. O exemplo a seguir mostra a estrutura do elemento .

```XML
...
    <query>
        <providers>
            <provider clsid=""/>    <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

### <a name="query-child-elements"></a>\<query> Elementos filho

A tabela a seguir descreve os elementos filho do elemento \<scope>.

| Elemento    | Descrição                                                                                                               | Valor                                                                                                                                                                                                                                                          |
|------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| providers  | Somente para uso interno. Não use.                                                                                        | n/d                                                                                                                                                                                                                                                            |
| Subconsultas | Somente para uso interno. Não use.                                                                                        | n/d                                                                                                                                                                                                                                                            |
| Escopo      | Identifica os locais a serem incluídos ou excluídos na pesquisa.                                                                 | Um caminho ou uma [ID de pasta conhecida](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) do local a ser incluído ou excluído. Esse elemento também pode especificar se a pesquisa deve incluir/excluir caminhos filho (uma pesquisa superficial ou profunda). |
| tipo de   | Identifica o tipo de arquivo (s) a ser pesquisado.                                                                             | Qualquer valor de System. Kind.                                                                                                                                                                                                                                         |
| condições | Especifica regras para filtrar resultados. Por exemplo, os resultados podem ser limitados a emails enviados por ou a uma pessoa específica. | andCondition, orCondition, não Condition, leafCondition.                                                                                                                                                                                                        |

### <a name="scope-element"></a>Elemento \<scope>

O \<scope> elemento identifica os locais a serem incluídos ou excluídos da pesquisa. O \<scope> elemento deve conter pelo menos um \<include> elemento filho presente e zero ou mais \<exclude> elementos. Os locais podem ser especificados como um caminho (as variáveis de ambiente têm suporte) ou como um [identificador de pasta conhecido](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid). Além disso, cada um desses locais pode ser especificado para ser pesquisado em profundidade ou superficial, definindo nonRecursive como "true" ou "false" (o padrão é recursivo). Partes da lista de locais incluída podem ser excluídas especificando-se elementos de exclusão.

O seguinte mostra um \<scope> elemento que pesquisará a pasta especial documentos, mas não seus filhos, o volume "e:" e seus filhos, mas não o diretório "E: \\ Windows" ou qualquer um de seus filhos:

```XML
...
    <query>
        ...
        <scope>
            <include knownFolder="{FDD39AD0-238F-46AF-ADB4-6C85480369C7}" nonRecursive="true"/>
            <include path="E:\"/>
            <exclude path="E:\Windows" nonRecursive="false"/>
        </scope>
        ...
    </query>
...
```

### <a name="kindlist-element"></a>Elemento \<kindList>

Esses elementos definem a União do "tipo" de itens que devem aparecer na biblioteca. Os valores válidos são:

- calendário
- comunicação
- contact
- documento
- email
- feed
- folder
- jogo
- instantmessage
- lança
- link
- filme
- music
- observação
- picture
- programa
- recordedtv
- searchfolder
- task
- video
- webhistory
- item
- outros

### <a name="conditions-element"></a>Elemento \<conditions>

As condições são filtros nos quais os resultados da pesquisa são comparados. Por exemplo, você pode filtrar os resultados que atendem a determinados critérios, como nome do autor ou tamanho do arquivo. O conjunto de condições é incorporado em uma árvore de condição única com branches lógicos AND, OR e NOT.

O exemplo a seguir mostra a estrutura do \<condition> elemento.

```XML
...
    <query>
        ...
        <conditions>
            <condition type="" ...>
                <attributes>
                    <attribute attributeID="" .../>
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

O tipo de condição pode ser um dos seguintes:

| Tipo          | Descrição                                 | Atributos disponíveis                               |
|---------------|---------------------------------------------|----------------------------------------------------|
| andCondition  | Conjunto de duas ou mais condições filho | n/d                                                |
| orCondition   | Disjunção de duas de mais condições filho | n/d                                                |
| Não condição  | Negação de uma condição filho               | n/d                                                |
| leafCondition | Compara uma propriedade com o valor                | Propriedade, propertyType, operador, valor, ValueType |

Os \<leafCondition> atributos do elemento identificam as propriedades e os valores nos quais os resultados são filtrados.

### <a name="example-conditions-element"></a>Exemplo: \<conditions> elemento

O exemplo a seguir filtra os resultados de todos os itens não lidos criados por João. Ou seja, a propriedade System. IsRead é false e a cadeia de caracteres "John" aparece nas propriedades System. Author ou System. ItemProperty.

```XML
...
    <query>
        ...
        <conditions>

            <condition type="andCondition">

                <condition type="leafCondition"
                           property="System.IsRead"
                           operator="eq"
                           value="FALSE"/>

                <condition type="orCondition">

                    <condition type="leafCondition"
                               property="System.Author"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                    <condition type="leafCondition"
                               property="System.ItemAuthors"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                </condition>

            </condition>

        </conditions>

    </query>
...
```

## <a name="properties-element"></a>Elemento \<properties>

O \<properties> elemento descreve as propriedades da pesquisa salva em si. Os arquivos de pesquisa salvos dão suporte a quatro propriedades: \<author> ,, \<kind> \<description> e \<tags> . Eles são apenas para uso interno.

## <a name="full-specification-of-the-search-ms-file-format"></a>Especificação completa do formato de arquivo Search-MS

Veja a seguir um exemplo do XML completo para um arquivo de pesquisa salvo.

```XML
<?xml version="1.0"?>

<persistedQuery version="1.0">

    <!-- The viewInfo section defines how results are displayed to the end user -->
    <viewInfo viewMode=""       <!-- details | icons | tiles -->
              iconSize=""       <!-- Integer -->
              stackIconSize=""  <!-- Do not use -->
              displayName=""    <!-- Do not use -->
              folderFlags=""    <!-- Do not use -->
              taskFlags=""      <!-- Do not use -->
              autoListFlags=""> <!-- Do not use -->

        <visibleColumns>
            <column viewField=""/>  <!-- System.[propertyname] -->
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/> <!-- Do not use -->
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>  <!-- Do not use -->
        </columnChooserColumns >

        <groupBy viewField=""       <!-- System.[propertyname] -->
                 direction=""/>     <!-- ascending | descending -->

        <stackList>
            <stack viewField=""/>   <!-- Do not use -->
        </stackList>

        <sortList>
            <sort viewField=""      <!-- System.[propertyname] -->
                  direction=""/>    <!-- ascending | descending -->
        </sortList>
    </viewInfo>

    <!-- The query section defines what gets searched (locations, file kinds) -->
    <query>
        <providers>
            <provider clsid=""/>          <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>

    <!-- The properties section identifies properties of the saved search file itself. -->
    <properties>
        ...             <!-- Do not use -->
    </properties>

</persistedQuery>
```

## <a name="examples-of-saved-searches"></a>Exemplos de pesquisas salvas

Veja a seguir exemplos de \* arquivos. Search-MS.

### <a name="recent-documentssearch-ms"></a>Documentos recentes. pesquisa-MS

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUZZXD-30NU" propertyType="wstr" />
        </conditions>
        <kindList>
            <kind name="Document"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recent-musicsearch-ms"></a>Música recente. pesquisa-MS

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUW-1WNNU" propertyType="wstr"/>
        </conditions>
        <kindList>
            <kind name="Music"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recently-shared-by-mesearch-ms"></a>Compartilhado recentemente por mim. pesquisa-MS

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <visibleColumns>
            <column viewField="System.ItemNameDisplay"/>
            <column viewField="System.DateModified"/>
            <column viewField="System.Keywords"/>
            <column viewField="System.SharedWith"/>
            <column viewField="System.ItemFolderPathDisplayNarrow"/>
        </visibleColumns>
        <frequentlyUsedColumns>
            <column viewField="System.Author"/>
            <column viewField="System.Kind"/>
            <column viewField="System.Size"/>
            <column viewField="System.Title"/>
            <column viewField="System.Rating"/>
        </frequentlyUsedColumns>
        <sortList>
            <sort viewField="System.SharedWith" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="andCondition">
                <condition type="leafCondition" property="System.IsShared" operator="eq" value="true"/>
                <condition type="leafCondition" property="System.FileOwner" operator="eq" value="[Me]"/>
            </condition>
        </conditions>
        <kindList>
            <kind name="item"/>
        </kindList>
        <scope>
            <include knownFolder="{5E6C858F-0E22-4760-9AFE-EA3317B67173}"/>
            <include knownFolder="{DFDF76A2-C82A-4D63-906A-5644AC457385}"/>
        </scope>
    </query>
</persistedQuery>
```
