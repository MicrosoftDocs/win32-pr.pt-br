---
description: Remove o registro de provedores.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Função de metalimpeza
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754617"
---
# <a name="countercleanup-function"></a>Função de metalimpeza

Remove o registro do provedor.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Seu provedor chama essa função. A função chama a função [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para remover o registro do provedor.

A ferramenta [**ctrpp**](ctrpp.md) gera essa função embutida quando você especifica o argumento **-o** . O nome da função inclui uma cadeia de caracteres de *prefixo* se você especificar o argumento **-prefix** (por exemplo, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 




