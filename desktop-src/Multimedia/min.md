---
title: macro min (Minwindef.h)
description: A macro min compara dois valores e retorna o menor. O tipo de dados pode ser qualquer tipo de dados numérico, assinado ou não assinado. O tipo de dados dos argumentos e o valor de retorno é o mesmo.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- min macro Windows Multimídia
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832adc4a4d326ca8e0689d1ca44ade2e0b77db770cabe6042e42c47e23a44f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985668"
---
# <a name="min-macro"></a>macro mín

A **macro min** compara dois valores e retorna o menor. O tipo de dados pode ser qualquer tipo de dados numérico, assinado ou não assinado. O tipo de dados dos argumentos e o valor de retorno é o mesmo.

## <a name="syntax"></a>Sintaxe


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value1* 
</dt> <dd>

Especifica o primeiro de dois valores.

</dd> <dt>

*value2* 
</dt> <dd>

Especifica o segundo de dois valores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o menor dos dois valores especificados.

## <a name="remarks"></a>Comentários

A **macro min** é definida da seguinte forma:


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Minwindef.h</dt> </dl> |



 

 





