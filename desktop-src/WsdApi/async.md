---
description: Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: elemento Async
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6cbc68d0a5dea30f4b4d179a54539ac3f9516a4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994953"
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



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




