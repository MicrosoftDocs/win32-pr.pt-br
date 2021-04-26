---
description: Gera declarações de implementação para funções de proxy para operações de tipo de porta.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: elemento functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508cbac6d220c0ebdee0c6306d5f8a8ab5f26770
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998813"
---
# <a name="functiondeclarations-element"></a>elemento functionDeclarations

Gera declarações de implementação para funções de proxy para operações de tipo de porta.

## <a name="usage"></a>Uso

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)<br/>         | Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.<br/> <br/>         |
| [**LostFocus**](events.md)<br/>       | Especifica se os eventos relacionados estão incluídos nas funções geradas.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.<br/> <br/> |
| [**operacional**](operation.md)<br/> | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse elemento gera declarações de funções de membro correspondentes às operações chamadas pelo contrato. Essas declarações estão em um formato apropriado para consumo por um compilador C++ e geralmente são usadas em arquivos. cpp.

Exemplo:

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




