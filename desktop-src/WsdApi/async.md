---
description: Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: elemento Async
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2597e0ed22fe9ccefa053891c0bd67ee76fae567847925de74faa1513de5faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049714"
---
# <a name="async-element"></a>elemento Async

Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.

## <a name="usage"></a>Uso

``` syntax
<async/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                         | Descrição                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                 | Gera declarações de implementação para funções de proxy para operações de tipo de porta.<br/> <br/> |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>           | Gera declarações IDL para funções de proxy para operações de tipo de porta.<br/> <br/>            |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/> | Gera implementações para funções de proxy para operações de tipo de porta.<br/> <br/>             |



## <a name="remarks"></a>Comentários

Os valores possíveis são 1 (operações assíncronas incluídas) e 0 (padrão, operações assíncronas excluídas).

Um proxy pode ter versões assíncronas e síncronas das mesmas operações.

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




