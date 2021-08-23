---
title: Tipo complexo ProviderType
description: Define um provedor e os metadados que ele usa para definir seus eventos. | Tipo complexo ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Tipo complexo ProviderType EventLog
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e48edd19d6ff9a547ce1698f81c89f780ffaa48f6312a656ef18664b39e78410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511266"
---
# <a name="providertype-complex-type"></a>Tipo complexo ProviderType

Define um provedor e os metadados que ele usa para definir seus eventos.

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                       | Type                                                                         | Descrição                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**canais**](eventmanifestschema-channels-providertype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)   | Define uma lista de canais para os quais os provedores podem registrar eventos.<br/>                                                                                                                                                                                      |
| [**Eventos**](eventmanifestschema-events-providertype-element.md)             | [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)     | Define uma lista de definições de evento dos eventos que o provedor pode registrar.<br/>                                                                                                                                                                       |
| **Filtros**                                                                   | [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)     | Define uma lista de filtros aos quais o provedor dá suporte. Você pode usar os filtros, como faria em nível e palavras-chave, para determinar se deseja gravar um evento. <br/> **Windows Server 2008 e Windows Vista:** Não há suporte até Windows 7.<br/> |
| [**Keywords**](eventmanifestschema-keywords-providertype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)   | Define uma lista de palavras-chave que categorizam eventos.<br/>                                                                                                                                                                                                 |
| [**Níveis**](eventmanifestschema-levels-providertype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)       | Define uma lista de níveis que especificam a severidade de um evento.<br/>                                                                                                                                                                                    |
| [**Mapas**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | Define uma lista de pares nome/valor que você pode referenciar na seção de modelo do manifesto.<br/>                                                                                                                                                 |
| [**namedQueries**](eventmanifestschema-namedqueries-providertype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)     | Não usado. Define uma lista de consultas nomeadas que consultam a cadeia de caracteres de mensagem de evento para um valor e executam uma ação especificada, se encontrada.<br/>                                                                                                                 |
| [**Opcodes**](eventmanifestschema-opcodes-providertype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)     | Define uma lista de opcodes que você pode usar para agrupar eventos dentro de uma tarefa.<br/>                                                                                                                                                                          |
| [**Tarefas**](eventmanifestschema-tasks-providertype-element.md)               | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)         | Define uma lista de tarefas que um provedor pode usar para agrupar eventos. Normalmente, você usa tarefas para agrupar eventos para um recurso ou componente do provedor.<br/>                                                                                              |
| [**Modelos**](eventmanifestschema-templates-providertype-element.md)       | [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md) | Define uma lista de modelos que especificam os dados a incluir com os eventos.<br/>                                                                                                                                                                      |



## <a name="attributes"></a>Atributos



| Nome                                | Tipo                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | Um GUID que identifica exclusivamente o provedor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Helplink                            | anyURI                                                            | A URL ou o link de ajuda do MS para o conteúdo que fornece informações sobre os eventos que o provedor gera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | O nome de exibição localizado para o provedor. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**stringTable**](eventmanifestschema-stringtable-resources-element.md) do manifesto. <br/>                                                                                                                                                                                                                                                                                                                           |
| messageFileName                     | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | O caminho completo para o arquivo que contém os recursos de mensagem localizados do provedor. O arquivo pode ser um arquivo executável ou um arquivo DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| name                                | anyURI                                                            | O nome do provedor. O nome deve estar no formato Componente *do Produto* -  - *da Empresa*.<br/> O nome não pode ter mais de 255 caracteres e não pode conter os caracteres: '>', '<', '&', '", ' \| ' \\ , ':', '', '?', ' ' ou caracteres com códigos menores \* que 31. Além disso, o nome deve seguir as restrições gerais em nomes de chave de arquivo e registro. Essas restrições podem ser encontradas em [Nomeando um arquivo](/windows/desktop/FileIO/naming-a-file)e limites de tamanho do [elemento do Registro.](/windows/desktop/SysInfo/registry-element-size-limits)<br/> |
| parameterFileName                   | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | O caminho completo para o arquivo que contém os recursos de cadeia de caracteres de parâmetro do provedor. O arquivo pode ser um arquivo executável ou um arquivo DLL. Você pode especificar mais de um arquivo de parâmetro separado por ponto e vírgula. O arquivo é pesquisado quando a cadeia de caracteres de mensagem de um evento contém uma cadeia de caracteres de parâmetro. Os parâmetros permitem fornecer cadeias de caracteres de inserção localizáveis. Consulte Comentários para obter mais informações.<br/>                                                                                                                                                |
| Resourcefilename                    | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | O caminho completo para o arquivo que contém os recursos de metadados do provedor. O arquivo pode ser um arquivo executável ou um arquivo DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | Somente para uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| símbolo                              | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar o GUID do provedor em seu aplicativo. O [**MC.exe (Compilador**](message-compiler--mc-exe-.md) de Mensagens) usa o símbolo para criar uma constante para o GUID do provedor no arquivo de header que o compilador gera.<br/>                                                                                                                                                                                                                                                                           |
| warnOnApplicationCompatibilityError | **xs:boolean**                                                    | Somente para uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>Comentários

O Windows Visualizador de Eventos (Eventvwr.exe) usará a cadeia de caracteres de mensagem localizada, se disponível; caso contrário, ele usará a cadeia de caracteres do atributo name.

Os caminhos para resourceFileName, messageFileName e parameterFileName podem conter variáveis de ambiente. Se você definir uma nova variável de ambiente a ser usada no caminho, deverá reiniciar o computador para que o serviço de log de eventos possa escolher a nova variável; caso contrário, o serviço não poderá encontrar os recursos do provedor.

A cadeia de caracteres de mensagem de um evento pode conter cadeias de caracteres de inserção e cadeias de caracteres de parâmetro. Uma cadeia de caracteres de inserção é do formato %*n*, em que *n* é um índice baseado em um que identifica um item de dados do modelo de dados do evento que você deseja inserir na mensagem. Uma cadeia de caracteres de parâmetro (consulte o atributo **parameterFileName)** é do formato %%*n*, em que n é o identificador de uma mensagem na tabela de mensagens. Se a cadeia de caracteres de mensagem do evento contivesse "%1 %%11 = %2 %%12" e os valores de item de dados para %1 e %2 fossem 8 e 2, respectivamente, e as cadeias de caracteres de parâmetro para %%11 e %%12 fossem "quarts" e "galões", respectivamente, a cadeia de caracteres formatada seria "8 quarts = 2 quartos".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

