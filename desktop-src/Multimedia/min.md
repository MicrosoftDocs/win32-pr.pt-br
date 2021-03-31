---
title: macro min (Minwindef. h)
description: A macro min compara dois valores e retorna o menor. O tipo de dados pode ser qualquer tipo de dados numéricos, assinados ou não assinados. O tipo de dados dos argumentos e o valor de retorno são os mesmos.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- Multimídia mín. de macro do Windows
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
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645256"
---
# <a name="min-macro"></a>macro mín

A macro **min** compara dois valores e retorna o menor. O tipo de dados pode ser qualquer tipo de dados numéricos, assinados ou não assinados. O tipo de dados dos argumentos e o valor de retorno são os mesmos.

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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o menor dos dois valores especificados.

## <a name="remarks"></a>Comentários

A macro **min** é definida da seguinte maneira:


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





