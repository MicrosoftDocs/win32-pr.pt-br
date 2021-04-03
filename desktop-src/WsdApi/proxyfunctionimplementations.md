---
description: Gera implementações para funções de proxy para operações de tipo de porta.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: elemento proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829502"
---
# <a name="proxyfunctionimplementations-element"></a>elemento proxyFunctionImplementations

Gera implementações para funções de proxy para operações de tipo de porta.

## <a name="usage"></a>Uso

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                     | Descrição                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)<br/>           | Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.<br/> <br/>         |
| [**LostFocus**](events.md)<br/>         | Especifica se os eventos relacionados estão incluídos nas funções geradas.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>   | Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.<br/> <br/> |
| [**operacional**](operation.md)<br/>   | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>     | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                                       |
| [**proxyClass**](proxyclass.md)<br/> | Especifica o nome da classe proxy do lado do cliente.<br/> <br/>                                               |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
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



 

 




