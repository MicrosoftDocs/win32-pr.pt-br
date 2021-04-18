---
description: Gera implementações para funções de stub para operações de tipo de porta.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813518"
---
# <a name="stubdefinitions-element"></a>elemento stubDefinitions

Gera implementações para funções de stub para operações de tipo de porta.

## <a name="usage"></a>Uso

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                         | Descrição                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**desalocador**](deallocator.md)<br/>                   | Especifica o tipo de desalocação a ser usado por uma função de stub.<br/> <br/>                                 |
| [**eventArg**](eventarg.md)<br/>                         | Especifica se argumentos de evento relacionados estão incluídos nas funções geradas.<br/> <br/>               |
| [**LostFocus**](events.md)<br/>                             | Especifica se os eventos relacionados estão incluídos nas funções geradas.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>                       | Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.<br/> <br/> |
| [**operacional**](operation.md)<br/>                       | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                                        |
| [**operationDeallocator**](operationdeallocator.md)<br/> | Especifica o tipo de desalocação a ser usado pela função de stub de uma operação.<br/> <br/>                    |
| [**portType**](porttype.md)<br/>                         | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                                       |
| [**serverClass**](serverclass.md)<br/>                   | Especifica o nome da classe de servidor do lado do host.<br/> <br/>                                                |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
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
| Pode estar vazio                        | Não            |



 

 




