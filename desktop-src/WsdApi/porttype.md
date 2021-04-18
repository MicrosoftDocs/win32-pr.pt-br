---
description: Especifica o tipo de porta para o qual o código deve ser gerado.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: elemento portType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a466ccdcfda133a2a314609e9698cd37c6bf31c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814005"
---
# <a name="porttype-element"></a>elemento portType

Especifica o tipo de porta para o qual o código deve ser gerado.

## <a name="usage"></a>Uso

``` syntax
<portType/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                                 | Descrição                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Gera declarações de implementação para funções de proxy para operações de tipo de porta.<br/> <br/>                                    |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Gera declarações IDL para funções de proxy para operações de tipo de porta.<br/> <br/>                                               |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Gera definições de estrutura C para tipos de mensagem.<br/> <br/>                                                                   |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.<br/> <br/>                                             |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Gera constantes C para tabelas de esquema XML para tipos de mensagem.<br/> <br/>                                                         |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Gera declarações de constante C para tipos de porta.<br/> <br/>                                                                      |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Gera constantes C para tipos de porta.<br/> <br/>                                                                                  |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Gera implementações para funções de proxy para operações de tipo de porta.<br/> <br/>                                                |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Gera declarações para funções de stub para operações de tipo de porta.<br/> <br/>                                                    |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Gera implementações para funções de stub para operações de tipo de porta.<br/> <br/>                                                 |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Gera declarações de implementação para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/>             |



## <a name="remarks"></a>Comentários

Por padrão, o código é gerado para todos os tipos de porta nos arquivos de entrada WSDL.

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




