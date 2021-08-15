---
description: Gera declarações IDL para funções de proxy para operações de tipo de porta.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f4bc12f0269e79142a4e55ad0cdc252b88b01959f6d18a6d4a4b5a8e72cde6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311728"
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



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




