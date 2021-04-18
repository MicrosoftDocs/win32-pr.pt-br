---
description: Direciona o gerador de código para gerar um arquivo e especifica o nome do arquivo de saída.
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: elemento de arquivo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc20f7d6853ccd52b231e19c99d60fe4b71d15b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793640"
---
# <a name="file-element"></a>elemento de arquivo

Direciona o gerador de código para gerar um arquivo e especifica o nome do arquivo de saída.

## <a name="usage"></a>Uso

``` syntax
<file
  name = "pathname string">
  child elements
</file>
```

## <a name="attributes"></a>Atributos



| Atributo           | Type                       | Obrigatório       | Descrição                                                                                                                         |
|---------------------|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **name**<br/> | Cadeia de nome do caminho<br/> | Yes<br/> | O nome de arquivo de saída do conteúdo gerado. A cadeia de caracteres do nome do arquivo deve incluir informações completas do caminho.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                 | Descrição                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CDATA**<br/>                                                                                    | As seções Text e CDATA são copiadas para o arquivo sem modificação. O código-fonte que não é uma função dos dados de entrada do contrato pode ser adicionado aos arquivos de saída usando seções de texto e CDATA.<br/> <br/> |
| [**enumerationValueDeclarations**](enumerationvaluedeclarations.md)<br/>                         | Gera declarações C para valores de todos os tipos enumerados.<br/> <br/>                                                                                                                                   |
| [**eventSourceBuilderDeclarations**](eventsourcebuilderdeclarations.md)<br/>                     | Gera declarações para funções que criam classes de origem de evento.<br/> <br/>                                                                                                                         |
| [**eventSourceBuilderImplementations**](eventsourcebuilderimplementations.md)<br/>               | Gera funções que criam classes de origem de evento.<br/> <br/>                                                                                                                                          |
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Gera declarações de implementação para funções de proxy para operações de tipo de porta.<br/> <br/>                                                                                                            |
| [**hostBuilderDeclaration**](hostbuilderdeclaration.md)<br/>                                     | Gera uma declaração para uma função que cria um host digitado.<br/> <br/>                                                                                                                              |
| [**hostBuilderImplementation**](hostbuilderimplementation.md)<br/>                               | Gera uma função que cria um host digitado.<br/> <br/>                                                                                                                                                |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Gera declarações IDL para funções de proxy para operações de tipo de porta.<br/> <br/>                                                                                                                       |
| [**incluir**](include.md)<br/>                                                                   | Inclui o conteúdo de uma macro ou arquivo na saída gerada.<br/> <br/>                                                                                                                              |
| [**IUnknownDeclarations**](iunknowndeclarations.md)<br/>                                         | Gera declarações para QueryInterface, AddRef e Release.<br/> <br/>                                                                                                                                 |
| [**IUnknownDefinitions**](iunknowndefinitions.md)<br/>                                           | Gera implementações para QueryInterface, AddRef e Release.<br/> <br/>                                                                                                                              |
| [**literalInclude**](literalinclude.md)<br/>                                                     | Coloca uma instrução de inclusão C ou IDL no código gerado. <br/> <br/>                                                                                                                                    |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Gera definições de estrutura C para tipos de mensagem.<br/> <br/>                                                                                                                                           |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.<br/> <br/>                                                                                                                     |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Gera constantes C para tabelas de esquema XML para tipos de mensagem.<br/> <br/>                                                                                                                                 |
| [**namespaceDeclarations**](namespacedeclarations.md)<br/>                                       | Gera declarações de C para tabelas de namespace.<br/> <br/>                                                                                                                                                 |
| [**namespaceDefinitions**](namespacedefinitions.md)<br/>                                         | Gera definições de C para tabelas de namespace.<br/> <br/>                                                                                                                                                  |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Gera declarações de constante C para tipos de porta.<br/> <br/>                                                                                                                                              |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Gera constantes C para tipos de porta.<br/> <br/>                                                                                                                                                          |
| [**proxyBuilderDeclarations**](proxybuilderdeclarations.md)<br/>                                 | Gera declarações para funções para criar proxies tipados.<br/> <br/>                                                                                                                                  |
| [**proxyBuilderImplementations**](proxybuilderimplementations.md)<br/>                           | Gera funções para criar proxies tipados.<br/> <br/>                                                                                                                                                   |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Gera implementações para funções de proxy para operações de tipo de porta.<br/> <br/>                                                                                                                        |
| [**relationshipMetadataDeclaration**](relationshipmetadatadeclaration.md)<br/>                   | Gera uma declaração de encaminhamento para os metadados de hospedagem especificados no elemento [**hostMetadata**](hostmetadata.md) . <br/> <br/>                                                                       |
| [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md)<br/>                     | Gera uma definição de constante C para os metadados de hospedagem especificados no elemento [**hostMetadata**](hostmetadata.md) . <br/> <br/>                                                                     |
| [**structDeclarations**](structdeclarations.md)<br/>                                             | Gera declarações de estrutura C para tipos conhecidos.<br/> <br/>                                                                                                                                            |
| [**structDefinitions**](structdefinitions.md)<br/>                                               | Gera definições de estrutura C para tipos conhecidos.<br/> <br/>                                                                                                                                             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Gera declarações para funções de stub para operações de tipo de porta.<br/> <br/>                                                                                                                            |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Gera implementações para funções de stub para operações de tipo de porta.<br/> <br/>                                                                                                                         |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Gera declarações de implementação para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/>                                                                         |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/>                                                                                    |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | As seções Text e CDATA são copiadas para o arquivo sem modificação. O código-fonte que não é uma função dos dados de entrada do contrato pode ser adicionado aos arquivos de saída usando seções de texto e CDATA.<br/> <br/> |
| [**thisModelMetadataDeclaration**](thismodelmetadatadeclaration.md)<br/>                         | Gera uma declaração de encaminhamento para a constante C para os metadados do fabricante especificados no elemento [**thisModelMetadata**](thismodelmetadata.md) .<br/> <br/>                                      |
| [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md)<br/>                           | Gera uma constante C para os metadados do fabricante especificados no elemento [**thisModelMetadata**](thismodelmetadata.md) .<br/> <br/>                                                                  |
| [**typeTableDeclarations**](typetabledeclarations.md)<br/>                                       | Gera declarações de constante C para tabelas de esquema XML para tipos conhecidos.<br/> <br/>                                                                                                                       |
| [**typeTableDefinitions**](typetabledefinitions.md)<br/>                                         | Gera constantes C para tabelas de esquema XML para tipos conhecidos.<br/> <br/>                                                                                                                                   |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  text, 
  CDATA, 
  namespaceDeclarations*, 
  namespaceDefinitions*, 
  structDeclarations*, 
  structDefinitions*, 
  typeTableDeclarations*, 
  typeTableDefinitions*, 
  thisModelMetadataDeclaration*, 
  thisModelMetadataDefinition*, 
  portTypeDeclarations*, 
  portTypeDefinitions*, 
  messageStructureDefinitions*, 
  messageTypeDeclarations*, 
  messageTypeDefinitions*, 
  idlFunctionDeclarations*, 
  subscriptionIdlFunctionDeclarations*, 
  functionDeclarations*, 
  subscriptionFunctionDeclarations*, 
  proxyFunctionImplementations*, 
  subscriptionProxyFunctionImplementations*, 
  stubDeclarations*, 
  stubDefinitions*, 
  enumerationValueDeclarations*, 
  include*, 
  IUnknownDeclarations*, 
  IUnknownDefinitions*, 
  relationshipMetadataDeclaration*, 
  relationshipMetadataDefinition*, 
  proxyBuilderDeclarations*, 
  proxyBuilderImplementations*, 
  hostBuilderDeclaration*, 
  hostBuilderImplementation*, 
  eventSourceBuilderDeclarations*, 
  eventSourceBuilderImplementations*, 
  literalInclude*
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                                     | Descrição                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentários

O nome do arquivo é determinado pelo valor do atributo Name ou do elemento filho. O conteúdo do arquivo é determinado pelos outros elementos filho, Text e CDATA no elemento **File** . Text e CDATA são copiados para o arquivo não modificado. Os elementos filho são substituídos pelo código gerado. Os elementos Text, CDATA e Child podem ocorrer em qualquer ordem e podem ser repetidos indefinidamente.

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




