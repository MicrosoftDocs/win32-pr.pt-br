---
description: Especifica se os parâmetros usados para passar informações de falha são incluídos em funções geradas.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: Elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 921a7dedfffbe7bfb3e402775258636ed9ccd3e74c72d65a5c76cea40d7ed4b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049673"
---
# <a name="faultinfo-element"></a>Elemento faultInfo

Especifica se os parâmetros usados para passar informações de falha são incluídos em funções geradas.

## <a name="usage"></a>Uso

``` syntax
<faultInfo/>
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
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Gera implementações para funções stub para operações de tipo de porta.<br/> <br/>              |



## <a name="remarks"></a>Comentários

Os valores possíveis são 1 (parâmetros de falha incluídos) e 0 (parâmetros de falha excluídos). Por padrão, os parâmetros de falha são excluídos.

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




