---
description: Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170001"
---
# <a name="faultinfo-element"></a>elemento faultInfo

Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.

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
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Gera implementações para funções de stub para operações de tipo de porta.<br/> <br/>              |



## <a name="remarks"></a>Comentários

Os valores possíveis são 1 (parâmetros de falha incluídos) e 0 (parâmetros de falha excluídos). Por padrão, os parâmetros de falha são excluídos.

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




