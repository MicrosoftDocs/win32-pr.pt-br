---
title: macro max (Minwindef.h)
description: A macro max compara dois valores e retorna o maior. O tipo de dados pode ser qualquer tipo de dados numérico, assinado ou não assinado. O tipo de dados dos argumentos e o valor de retorno é o mesmo.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- max macro Windows Multimídia
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc592fcc588c14ee04c1f595c5b5bc95c860b2ab0b761906886010db478d5f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138642"
---
# <a name="max-macro"></a>macro máx

A **macro** max compara dois valores e retorna o maior. O tipo de dados pode ser qualquer tipo de dados numérico, assinado ou não assinado. O tipo de dados dos argumentos e o valor de retorno é o mesmo.

## <a name="syntax"></a>Sintaxe


```C++
 max(
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

O valor de retorno é o maior dos dois valores especificados.

## <a name="remarks"></a>Comentários

A **macro** max é definida da seguinte forma:


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Minwindef.h</dt> </dl> |



 

 





