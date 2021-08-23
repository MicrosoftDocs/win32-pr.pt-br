---
description: Especifica uma operação para a qual o código deve ser gerado.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: elemento operation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab38721d1eb0d32c2ed7209dde872a83b29a523942ac7b91ca76f479ce5d51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502186"
---
# <a name="operation-element"></a>elemento operation

Especifica uma operação para a qual o código deve ser gerado.

## <a name="usage"></a>Uso

``` syntax
<operation/>
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
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Gera declarações constantes C para tabelas de esquema XML para tipos de mensagem.<br/> <br/>                                             |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Gera constantes C para tabelas de esquema XML para tipos de mensagem.<br/> <br/>                                                         |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Gera declarações constantes C para tipos de porta.<br/> <br/>                                                                      |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Gera constantes C para tipos de porta.<br/> <br/>                                                                                  |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Gera implementações para funções de proxy para operações de tipo de porta.<br/> <br/>                                                |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Gera declarações para funções stub para operações de tipo de porta.<br/> <br/>                                                    |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Gera implementações para funções stub para operações de tipo de porta.<br/> <br/>                                                 |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Gera declarações de implementação para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.<br/> <br/>             |



## <a name="remarks"></a>Comentários

Qualquer número de operações pode ser especificado. Se nenhuma operação for especificada, o código será gerado para todas as operações em todos os tipos de porta relevantes. O uso **do elemento** operation limitará os métodos gerados aos contidos na operação.

Por exemplo, uma impressora dá suporte a essas operações entre outras:

-   **PrintJobByPost**
-   **PrintJobByReference**
-   **CancelJob**
-   **GetJobElements**
-   **GetActiveJobs**
-   **GetJobHistory**
-   **SubscribeToPrinterConfigChange**
-   **UnsubscribeToPrinterConfigChange**

No entanto, para incluir apenas os métodos relacionados às operações **PrintJobByPost** e **GetJobElements,** o script de geração de código usaria os elementos [**idlFunctionDeclarations**](idlfunctiondeclarations.md) da seguinte maneira:

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

Isso gera declarações de função idl para todos os métodos associados às duas operações (por exemplo, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** e **EndGetJobElements**).

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




