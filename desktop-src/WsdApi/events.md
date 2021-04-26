---
description: Especifica se os eventos relacionados estão incluídos nas funções geradas.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995923"
---
# <a name="events-element"></a>elemento Events

Especifica se os eventos relacionados estão incluídos nas funções geradas.

## <a name="usage"></a>Uso

``` syntax
<events/>
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
| [**stubDeclarations**](stubdeclarations.md)<br/>                         | Gera declarações para funções de stub para operações de tipo de porta.<br/> <br/>                 |
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Gera implementações para funções de stub para operações de tipo de porta.<br/> <br/>              |



## <a name="remarks"></a>Comentários

Os valores possíveis são 1 (eventos incluídos) e 0 (padrão, eventos excluídos).

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




