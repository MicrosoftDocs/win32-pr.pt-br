---
description: Processo de consulta no Windows Search
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Processo de consulta no Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3585f2cca2a6d5d8548a85ae8fac759ec94b4fa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117324"
---
# <a name="querying-process-in-windows-search"></a>Processo de consulta no Windows Search

Este tópico é organizado da seguinte maneira:

-   [Sobre a consulta no Windows Search](#about-querying-in-windows-search)
    -   [Consultas locais e remotas](#local-and-remote-queries)
    -   [Visão geral da API de consulta estruturada](#structured-query-api-overview)
-   [Cenários de consulta](#querying-scenarios)
    -   [Extração de condição e análise de consulta](#condition-extraction-and-query-parsing)
    -   [Consultando o índice](#querying-the-index)
-   [Tópicos relacionados](#related-topics)

## <a name="about-querying-in-windows-search"></a>Sobre a consulta no Windows Search

A consulta no Windows Search baseia-se nas quatro abordagens a seguir:

-   [Sintaxe de consulta avançada](-search-3x-advancedquerysyntax.md) (AQS)
-   Sintaxe de consulta natural (NQS)
-   SQL (Structured Query Language)
-   Interfaces de consulta estruturadas

AQS é a sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir os parâmetros de pesquisa. O AQS é voltado principalmente para o usuário e pode ser usado por usuários para criar consultas AQS, mas também pode ser usado por desenvolvedores para criar consultas programaticamente. No Windows 7, o AQS canônico foi introduzido e deve ser usado para gerar consultas AQS programaticamente. No Windows 7 e posterior, uma opção de menu de atalho pode estar disponível com base no fato de uma condição AQS ser atendida. Para obter mais informações, consulte "obtendo comportamento dinâmico para verbos estáticos usando a sintaxe de consulta avançada" em [criando manipuladores de menu de contexto](../shell/context-menu-handlers.md). As consultas AQS podem ser limitadas a tipos específicos de arquivos, que são conhecidos como tipos de arquivo. Para obter mais informações, consulte [tipos de arquivo e associações](../shell/fa-intro.md). Para obter a documentação de referência sobre as propriedades relevantes, consulte [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).

NQS é uma sintaxe de consulta mais relaxada do que o AQS e é semelhante ao idioma humano. NQS pode ser usado pelo Windows Search para consultar o índice se NQS for selecionado em vez do padrão, AQS.

SQL é uma linguagem de texto que define consultas. O SQL é comum entre muitas tecnologias de banco de dados diferentes. O Windows Search usa o SQL, implementa um subconjunto dele e o estende adicionando elementos ao idioma. O Windows Search SQL estende a sintaxe de consulta de banco de dados SQL-92 e SQL-99 padrão para aprimorar sua utilidade com pesquisas baseadas em texto. Todos os recursos do Windows Search SQL são compatíveis com o Windows Search no Windows XP e no Windows Server 2003 e posterior. Para obter mais informações sobre o SQL Search do Windows, consulte [consultando o índice com a sintaxe SQL do Windows Search](-search-sql-windowssearch-entry.md)e [visão geral da sintaxe SQL do Windows Search](-search-sql-ovwofsearchquery.md).

As APIs de consulta estruturada são descritas posteriormente neste tópico. Para obter a documentação de referência sobre as APIs de consulta estruturada, consulte [consultando interfaces](-search-querying-interfaces-entry-page.md). Interfaces como [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) ajudam a construir cadeias de caracteres SQL de um conjunto de valores de entrada. Essa interface converte as consultas de usuário AQS no SQL Search do Windows e especifica as restrições de consulta que podem ser expressas em SQL, mas não em AQS. O [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) também obtém uma cadeia de conexão OLE DB para se conectar ao banco de dados do Windows Search.

### <a name="local-and-remote-queries"></a>Consultas locais e remotas

Você pode executar suas consultas de forma local ou remota. Uma consulta local usando a [cláusula from](-search-sql-from.md) é mostrada no exemplo a seguir. Uma consulta local pesquisa apenas o catálogo SystemIndex local.


```
FROM SystemIndex
```



Uma consulta remota usando a [cláusula from](-search-sql-from.md) é mostrada no exemplo a seguir. Adicionar ComputerName transforma o exemplo anterior em uma consulta remota.


```
FROM [<ComputerName>.]SystemIndex
```



Por padrão, o Windows XP e o Windows Server 2003 não têm o Windows Search instalado. Somente o Windows Search 4 (WS4) fornece suporte de consulta remota. As versões anteriores do Windows Desktop Search (WDS), como 3, 1 e anteriores, não oferecem suporte a consultas remotas. Com o Windows Explorer, você pode consultar o índice local de um computador remoto para itens do sistema de arquivos (itens manipulados pelo protocolo "file:").

Para recuperar um item pela consulta remota, o item deve atender aos seguintes requisitos:

-   Ser acessível por meio do caminho UNC (Convenção de nomenclatura universal).
-   Existem no computador remoto ao qual o cliente tem acesso.
-   Tenha sua segurança definida para permitir que o cliente tenha acesso de leitura.

O Windows Explorer tem recursos para compartilhar itens, incluindo um compartilhamento "público" ( \\ \\ público de máquina... \\ \\ ) no **centro de rede e compartilhamento** e um compartilhamento de "usuários" ( \\ \\ usuários do computador \\ \\ ...) para itens compartilhados por meio do assistente de compartilhamento. Depois de compartilhar as pastas, você pode consultar o índice local especificando o nome da máquina remota do computador na cláusula FROM e um caminho UNC no computador remoto na cláusula SCOPE. Uma consulta remota usando as cláusulas FROM e SCOPE é mostrada no exemplo a seguir.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



Os exemplos fornecidos aqui usam SQL.

### <a name="structured-query-api-overview"></a>Visão geral da API de consulta estruturada

Uma consulta estruturada fornece a capacidade de pesquisar informações por combinações booleanas de consultas em propriedades individuais. Neste tópico, descrevemos a funcionalidade das APIs e métodos de consulta estruturada mais importantes. Para obter a documentação de referência sobre as APIs de consulta estruturada, consulte [consultando interfaces](-search-querying-interfaces-entry-page.md).

### <a name="iqueryparser"></a>IQueryParser

O método [**IQueryParser::P grosseira**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) analisa uma cadeia de caracteres de entrada do usuário e produz uma interpretação na forma de um [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution). Se o parâmetro *pCustomProperties* desse método não for nulo, ele será uma enumeração de objetos [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) (um para cada propriedade personalizada reconhecida). Os outros métodos [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) permitem que o aplicativo defina várias opções, como localidade, um esquema, um separador de palavras e manipuladores para vários tipos de entidades nomeadas. [**IQueryParser:: Getschemaprovider**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) retorna uma interface [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) para procurar o esquema carregado.

### <a name="iquerysolution--iconditionfactory"></a>IQuerySolution : IConditionFactory

A interface [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) fornece todas as informações sobre o resultado da análise de uma cadeia de caracteres de entrada. Como **IQuerySolution** também é uma interface [**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) , nós de árvore de condição adicionais podem ser criados. O método [**IQuerySolution:: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) produz uma árvore de condição para a interpretação. **IQuerySolution:: GetQuery** também retorna o tipo semântico.

### <a name="iconditionfactory"></a>IConditionFactory

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) cria nós de árvore de condição. Se o parâmetro de *simplificação* de [**IConditionFactory:: MakeNot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) for **Variant \_ true**, o [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) resultante será simplificado e não precisará ser um nó de negação. Se o parâmetro *pSubConditions* de [**IConditionFactory:: MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) não for nulo, esse parâmetro deverá ser uma enumeração de objetos [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) e se tornará subárvores. [**IConditionFactory:: MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) constrói um nó folha com um nome de propriedade, uma operação e um valor especificados. A cadeia de caracteres *no parâmetro* nametype deve ser o nome de um tipo semântico do esquema. Se o parâmetro *Expand* for **Variant \_ true** e a propriedade for virtual, a árvore de condição resultante normalmente será uma disjunção resultante da expansão da propriedade para seus constituintes definidos. Se não for NULL, os parâmetros *pPropertyNameTerm*, *pOperatorTerm* e *pValueTerm* deverão identificar os termos que indicam a propriedade, a operação e o valor.

### <a name="icondition--ipersiststream"></a>ICondition: IPersistStream

A interface [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) é um único nó em uma árvore de condição. O nó pode ser um nó de negação, nó, ou nó ou um nó folha. Para um nó não folha [**ICondition:: GetSubConditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) retorna uma enumeração das subárvores. Para um nó folha, os seguintes métodos de [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) retornam os seguintes valores:

-   [**GetComparisonInfo**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) retorna o nome da propriedade, a operação e o valor.
-   [**Getvaluetype**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) retorna o tipo semântico do valor, que foi specificied no parâmetro *pszValueType* de [**IConditionFactory:: MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf).
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) retorna uma forma de cadeia de caracteres do valor. (Se o valor já era uma cadeia de caracteres, esse formulário será normalizado com relação a casos, acentos e assim por diante.)
-   [**GetInputTerms**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) retorna informações sobre quais partes da sentença de entrada geraram o nome da propriedade, a operação e o valor.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) retorna uma cópia profunda de uma árvore de condição.

### <a name="irichchunk"></a>IRichChunk

Cada objeto [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) identifica um token span e uma cadeia de caracteres. **IRichChunk** é uma interface do utilitário que representa informações sobre um Span (normalmente um intervalo de tokens) identificado por uma posição inicial e um comprimento. Essas informações de span incluem uma cadeia de caracteres e/ou uma **variante**.

### <a name="iconditiongenerator"></a>IConditionGenerator

A interface [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) é fornecida pelo aplicativo para lidar com o reconhecimento e a geração de árvore de condição para um tipo de entidade nomeada. Um gerador de condição é fornecido a um [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) por meio de [**IQueryParser:: SetMultiOption**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption). [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) chama [**IConditionGenerator:: Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) com um [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) para o esquema atualmente carregado. Isso permite que o [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) Obtenha informações de esquema necessárias. Ao analisar uma cadeia de caracteres de entrada, **IQueryParser** chama o método [**IConditionGenerator:: RecognizeNamedEntities**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) de cada [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), para que a ocorrência de entidades nomeadas que ele reconhece na cadeia de caracteres de entrada possa ser relatada. O **IQueryParser** pode usar a localidade atual e deve usar a geração de tokens da entrada, pois ela precisa relatar as extensões de token de quaisquer entidades nomeadas.

Quando [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) está prestes a emitir um nó folha, e o tipo semântico do valor corresponde ao tipo de entidade nomeada para um [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), **IQueryParser** chama [**IConditionGenerator:: GenerateforLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) com as informações para o nó a ser gerado. Se [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) retornar S \_ OK, ele deverá retornar uma árvore de condição (que não precisa ser um nó folha) e informar **IQueryParser** se deve suprimir a interpretação de cadeia de caracteres alternativa que normalmente geraria como uma precaução.

### <a name="itokencollection"></a>ITokenCollection

O método [**ITokenCollection:: NumberOfTokens**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) retorna o número de tokens. [**ITokenCollection:: GetToken**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) retorna informações sobre o símbolo *i*. O início e o comprimento são posições de caracteres na cadeia de caracteres de entrada. O texto retornado será não nulo somente se houver um texto substituindo os caracteres da cadeia de caracteres de entrada. Isso é usado, por exemplo, para substituir um traço na cadeia de caracteres de entrada e não quando esse traço está em um contexto onde ele deve ser interpretado como uma negação.

### <a name="inamedentitycollector"></a>INamedEntityCollector

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) chama [**INamedEntityCollector:: Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) para cada entidade nomeada reconhecida. As extensões são spans de token. Ele sempre deve ser o caso que *beginSpan* ? *beginActual*  <  *endreal* ? *endspan*. *beginSpan* e *endspan* podem ser diferentes de *beginActual* e *endreal* se a entidade nomeada começa e/ou termina com tokens semanticamente insignificantes, como aspas (que são, no entanto, cobertas pela entidade nomeada). O valor deve ser expresso como uma cadeia de caracteres e, subsequentemente, aparecerá em uma chamada para [**IConditionGenerator:: GenerateForLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf).

### <a name="ischemaprovider"></a>ISchemaProvider

A interface [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) pode ser usada para procurar um esquema carregado para entidades (tipos) e relações (Propriedades). Veja a seguir os métodos individuais:

-   As [**entidades**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) retornam uma enumeração de cada entidade ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) no esquema.
-   [**RootEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) retorna a entidade raiz do esquema. Para um esquema simples, o tipo principal de cada [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) é retornado.
-   [**GetEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) localiza uma entidade por nome e retorna S \_ false se não houver essa entidade no esquema.
-   [**Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) retorna uma enumeração de interfaces [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) .

### <a name="ientity"></a>IEntity

A interface [**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) é uma entidade de esquema que representa um tipo que tem um nome, tem um número de relações nomeadas para outros tipos (Propriedades) e deriva de uma entidade base. Veja o que seus métodos individuais fazem:

-   [**IEntity:: Relationships**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) retorna uma enumeração de objetos [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) , um para cada relação de saída desse tipo. Cada relação de saída de uma entidade tem um nome.
-   [**IEntity:: GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) localiza uma relação por nome e retorna S \_ false se não houver tal relação para essa entidade.
-   [**IEntity:: Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) retorna uma enumeração de interfaces [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , uma para cada par de metadados desta entidade.
-   [**IEntity::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) retorna uma frase padrão para facilitar a geração de uma redefinição de AQS ou nQS de uma árvore de condição.

### <a name="irelationship"></a>IRelationship

A interface [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) representa uma relação entre duas entidades: uma origem e um destino. Veja a seguir os métodos individuais:

-   [**IRelationship:: Isreal**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) relata se uma relação é real. Por exemplo, se A entidade A derivar da entidade B e herdar uma relação chamada R a partir dela, uma pode ainda ter sua própria relação chamada R. No entanto, a relação beween A e R deve ter o mesmo tipo de destino que o de B, e a única razão para ela existir é armazenar os metadados específicos para B. Essa relação de B é mencionada como real.
-   [**IRelationship:: das**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) retorna uma enumeração de interfaces [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , uma para cada par de metadados desta entidade.
-   [**IRelationship::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) retorna a frase padrão a ser usada para essa relação em reestado. Cada relação tem uma frase padrão que a denota para facilitar a geração de uma redefinição de AQS ou NQS de uma árvore de condição.

### <a name="imetadata"></a>IMetaData

Os metadados são pares chave-valor que são associados a uma entidade, a uma relação ou ao esquema inteiro. Como as chaves não são necessariamente exclusivas, uma coleção de metadados pode ser considerada como um mapa múltiplo. [**IMetadata:: GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) é chamado para recuperar a chave e o valor de um par de refletir.

## <a name="querying-scenarios"></a>Cenários de consulta

Os cenários a seguir descrevem o uso de APIs de consulta estruturada no Windows Search em cenários de consulta comuns, como a criação de uma árvore de condição e a consulta do índice.

### <a name="condition-extraction-and-query-parsing"></a>Extração de condição e análise de consulta

Quando uma consulta é criada, seu escopo é definido informando ao sistema onde Pesquisar. Isso restringe os resultados da pesquisa. Depois que o escopo é definido, um filtro é aplicado e um conjunto de filtros é retornado. Os resultados da pesquisa são restritos pela criação de uma árvore de condição com nós folha, semelhante a um grafo. Essas condições são extraídas. Uma árvore de condição é uma combinação booleana (e, ou, não) de condições folha, cada uma das quais relaciona uma propriedade, por meio de uma operação, a um valor. Um nó folha representa uma restrição em uma única propriedade para um valor por meio de algumas operações.

Uma restrição de filtro requer uma expressão lógica que descreva a restrição. Definir essa expressão começa com a interface [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) , que é usada para criar um único nó em uma árvore de condição. Como há apenas uma condição no exemplo a seguir, a árvore não é alterada.


```C++
    
    [
        object,
        uuid(0FC988D4-C935-4b97-A973-46282EA175C8),
        pointer_default(unique)
    ]
    interface ICondition : IPersistStream
    {
        HRESULT GetConditionType([out, retval] CONDITION_TYPE* pNodeType);
        HRESULT GetSubConditions([in] REFIID riid, [out, retval, iid_is(riid)] void** ppv);
        [local] HRESULT GetComparisonInfo([out, annotation("__deref_opt_out")] LPWSTR *ppszPropertyName, [out, annotation("__out_opt")] CONDITION_OPERATION *pOperation, [out, annotation("__out_opt")] PROPVARIANT *pValue);
        HRESULT GetValueType([out, retval] LPWSTR* ppszValueTypeName);
        HRESULT GetValueNormalization([out, retval] LPWSTR* ppszNormalization);
        [local] HRESULT GetInputTerms([out, annotation("__out_opt")] IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] IRichChunk** ppValueTerm);
        HRESULT Clone([out, retval] ICondition** ppc);
    };


```



Se houver mais de uma condição de filtro, então e outros operadores boolianos serão usados para obter uma única árvore. E-árvores e árvores representam conjunção e disjunções de suas subárvores. Uma árvore NOT representa a negação de sua única subárvore. O AQS fornece uma abordagem de texto para alcançar expressões lógicas com operadores boolianos e é geralmente mais simples.

No próximo exemplo, convertemos a árvore de condição ([**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) no formato visual. O analisador de consulta, usando a interface [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) , converte o [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) em uma cadeia de caracteres de consulta Rich Text formatada (RTF). O método [**IQueryParser:: RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) retorna o texto da consulta, enquanto o método [**IQueryParser::P grosseira**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) produz uma interface [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) . O exemplo a seguir mostra como fazer tudo isso.


```C++
    [
        object,
        uuid(2EBDEE67-3505-43f8-9946-EA44ABC8E5B0),
        pointer_default(unique)
    ]
    interface IQueryParser : IUnknown
    {
        HRESULT Parse([in] LPCWSTR pszInputString, [in] IEnumUnknown* pCustomProperties, [out, retval] IQuerySolution** ppSolution);
        HRESULT SetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [out, retval] PROPVARIANT* pOptionValue);
        HRESULT SetMultiOption([in] STRUCTURED_QUERY_MULTIOPTION option, [in] LPCWSTR pszOptionKey, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetSchemaProvider([out, retval] ISchemaProvider** ppSchemaProvider);
        HRESULT RestateToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszQueryString);
        HRESULT ParsePropertyValue([in] LPCWSTR pszPropertyName, [in] LPCWSTR pszInputString, [out, retval] IQuerySolution** ppSolution);
        HRESULT RestatePropertyValueToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszPropertyName, [out] LPWSTR* ppszQueryString);
    };

```



A principal entrada de [**IQueryParser::P grosseira**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) é uma cadeia de caracteres de entrada do usuário a ser analisada, mas o aplicativo também pode informar o analisador de consulta de quaisquer propriedades reconhecidas na entrada (a partir da sintaxe específica do aplicativo). A saída de **IQueryParser::P grosseira** é um [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution), que fornece todas as informações referentes a essa invocação de análise. Há métodos para obter a cadeia de caracteres de entrada, como a cadeia de caracteres de entrada foi indexada, quaisquer erros de análise e a consulta analisada como árvore de condição, representada por um [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition). O exemplo a seguir mostra...


```C++
    [
        object,
        uuid(D6EBC66B-8921-4193-AFDD-A1789FB7FF57),
        pointer_default(unique)
    ]
    interface IQuerySolution : IConditionFactory
    {
        [local] HRESULT GetQuery([out, annotation("__out_opt")] ICondition** ppQueryNode, [out, annotation("__out_opt")] IEntity** ppMainType);
        HRESULT GetErrors([in] REFIID riid, [out, retval, iid_is(riid)] void** ppParseErrors);
        [local] HRESULT GetLexicalData([out, annotation("__deref_opt_out")] LPWSTR* ppszInputString, [out, annotation("__out_opt")] ITokenCollection** ppTokens, [out, annotation("__out_opt")] LCID* pLocale, [out, annotation("__out_opt")] IUnknown** ppWordBreaker);
    }    

    

```



No exemplo anterior, [**IQuerySolution:: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) poderia obter qualquer informação sobre a consulta, incluindo o texto original, tokens que compõem o texto ou a árvore de condição. Exemplos de valores de consulta retornados possíveis são listados na tabela a seguir.



| Exemplos de valores de consulta retornados                        | Descrição                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | O texto da consulta que [**IQueryParser:: RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) retorna |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | A quebra de tokens                                                                                  |
| ![uma árvore de condição não resolvida](images/queryvalues1.png) | Uma árvore de condição não resolvida                                                                              |



 

A árvore de condição inicial retornada não é resolvida. Em uma árvore de condição não resolvida, as referências de data e hora, como `date:yesterday` , não são convertidas em tempo absoluto. Além disso, as propriedades virtuais não são expandidas. Propriedades virtuais são propriedades que atuam como agregações de várias propriedades.

Por exemplo, a consulta `kind:email from:reljai` produz as seguintes árvores de condição não resolvidas e resolvidas. A árvore de condição não resolvida está à esquerda e a árvore de condição resolvida está à direita.

![árvores de condição não resolvidas e resolvidas](images/conditiontree.png)

A árvore resolvida pode ser obtida chamando [**IConditionFactory:: resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve). No entanto, passar [**SQRO não \_ \_ resolver \_ DateTime**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) deixa a data e a hora não resolvidas. Há vantagens em uma árvore de condição não resolvida, porque uma árvore de condição não resolvida contém informações sobre a consulta. Cada nó folha aponta para os tokens retornados por [**IQuerySolution:: GetLexicalData**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata), que correspondem à propriedade, ao operador e ao valor ao usar a interface [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) . O exemplo a seguir mostra...


```C++
    interface ITokenCollection : IUnknown
    {
        HRESULT NumberOfTokens(ULONG* pCount);
        HRESULT GetToken([in] ULONG i, [out, annotation("__out_opt")] ULONG* pBegin, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz);
    };

ICondition:: GetInputTerms([out, annotation("__out_opt")] 
IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] 
IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] 
IRichChunk** ppValueTerm);

    interface IRichChunk : IUnknown
    {
        HRESULT GetData([out, annotation("__out_opt")] ULONG* pFirstPos, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz, [out, annotation("__out_opt")] PROPVARIANT* pValue);
    }
```



### <a name="querying-the-index"></a>Consultando o índice

Há várias abordagens para consultar o índice. Algumas são baseadas no SQL e outras são baseadas em AQS. Você também pode consultar o índice do Windows Search programaticamente usando a [consulta de interfaces](./-search-querying-interfaces-entry-page.md). Há três interfaces que são específicas para consultar o índice: [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)e [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Para obter informações conceituais, consulte [consultando o índice programaticamente](-search-3x-wds-qryidx-overview.md).

Você pode desenvolver um componente ou classe auxiliar para consultar o índice usando a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . Essa interface é implementada como uma classe auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) e é obtida chamando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Para obter informações conceituais, consulte [consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md).

O [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) permite que você:

-   Obtenha uma cadeia de conexão OLE DB para se conectar ao banco de dados de pesquisa do Windows.
-   Converta as consultas de usuário do AQS no SQL do Windows Search.
-   Especifique as restrições de consulta que podem ser expressas em SQL, mas não em AQS.

A priorização de indexação e os eventos de conjunto de linhas têm suporte no Windows 7 e versões posteriores. Com [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) , há uma pilha de prioridade que permite que o cliente solicite que os escopos usados em uma determinada consulta sejam maiores que a prioridade normal. O [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) fornece notificação de alterações em itens em conjuntos de linhas, incluindo a adição de novos itens, a exclusão de itens e a modificação de dados do item. O uso de notificações de eventos de conjunto de linhas garante que os resultados de consultas existentes sejam os mais atualizados possíveis. Para obter informações conceituais, consulte [indexando a priorização e eventos de conjunto de linhas no Windows 7](indexing-prioritization-and-rowset-events.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Indexação, consulta e notificações no Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[O que está incluído no índice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo de indexação no Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Processo de notificações no Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisitos de formatação de URL](url-formatting-requirements.md)
</dt> </dl>

 

 
