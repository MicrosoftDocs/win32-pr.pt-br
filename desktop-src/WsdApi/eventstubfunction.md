---
description: Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações de notificação.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: elemento eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe353f43d02eec68f29f3075cc445c1314c9762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813542"
---
# <a name="eventstubfunction-element"></a>elemento eventStubFunction

Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações de notificação.

## <a name="usage"></a>Uso

``` syntax
<eventStubFunction/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                       | Descrição                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [**portTypeDefinitions**](porttypedefinitions.md)<br/> | Gera constantes C para tipos de porta.<br/> <br/> |



## <a name="remarks"></a>Comentários

As referências de função de stub estão em cenários de cliente para operações de notificação (eventos).

Os valores válidos para esse elemento são 1 (referências de função TRUE/stub incluídas) e 0 (FALSE/nenhuma referência de função de stub incluída).

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




