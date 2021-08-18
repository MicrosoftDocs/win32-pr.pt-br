---
description: Remove o registro de provedores.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Função CounterCleanup
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
ms.openlocfilehash: fe06923849a12609b6662505df94c927c3d9dfd4aeb8bc6a42bd6a225e042ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011364"
---
# <a name="countercleanup-function"></a>Função CounterCleanup

Remove o registro do provedor.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Seu provedor chama essa função. A função chama a [**função PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para remover o registro do provedor.

A [**ferramenta CTRPP**](ctrpp.md) gera essa função em linha quando você especifica o **argumento -o.** O nome da função incluirá uma cadeia de caracteres *de prefixo* se você especificar o **argumento -prefix** (por exemplo, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



 

 




