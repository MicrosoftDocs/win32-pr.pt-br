---
description: Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: elemento subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829631"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a>elemento subscriptionIdlFunctionDeclarations

Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.

## <a name="usage"></a>Uso

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a>Atributos



| Atributo                 | Type               | Obrigatório      | Descrição                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **ampliá**<br/> | booleano<br/> | No<br/> | A capacidade de adicionar pontos de extensibilidade a funções e interfaces. Esse valor é sempre definido como true.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                           | Descrição                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | Especifica o nome da interface de notificação usada com assinaturas de evento.<br/> <br/> |
| [**operacional**](operation.md)<br/>                         | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                       |
| [**portType**](porttype.md)<br/>                           | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                      |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




