---
description: Gera declarações IDL para funções de proxy para operações de tipo de porta.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994733"
---
# <a name="idlfunctiondeclarations-element"></a>elemento idlFunctionDeclarations

Gera declarações IDL para funções de proxy para operações de tipo de porta.

## <a name="usage"></a>Uso

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)<br/>         | Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.<br/> <br/>         |
| [**eventArg**](eventarg.md)<br/>   | Especifica se argumentos de evento relacionados estão incluídos nas funções geradas.<br/> <br/>               |
| [**LostFocus**](events.md)<br/>       | Especifica se os eventos relacionados estão incluídos nas funções geradas.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.<br/> <br/> |
| [**operacional**](operation.md)<br/> | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
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

Esse elemento gera declarações de funções de membro correspondentes às operações chamadas pelo contrato. Essas declarações estão em um formato apropriado para consumo pelo compilador MIDL e são geralmente usadas em arquivos. idl.

Exemplo:

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




