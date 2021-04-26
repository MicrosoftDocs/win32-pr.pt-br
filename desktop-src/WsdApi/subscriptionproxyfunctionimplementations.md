---
description: Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: elemento subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995313"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a>elemento subscriptionProxyFunctionImplementations

Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.

## <a name="usage"></a>Uso

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a>Atributos



| Atributo                 | Type               | Obrigatório      | Descrição                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **ampliá**<br/> | booleano<br/> | Não<br/> | A capacidade de adicionar pontos de extensibilidade a funções e interfaces. Esse valor é sempre definido como true.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                           | Descrição                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | Especifica o nome da interface de notificação usada com assinaturas de evento.<br/> <br/> |
| [**operacional**](operation.md)<br/>                         | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                       |
| [**portType**](porttype.md)<br/>                           | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                      |
| [**proxyClass**](proxyclass.md)<br/>                       | Especifica o nome da classe proxy do lado do cliente.<br/> <br/>                              |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




