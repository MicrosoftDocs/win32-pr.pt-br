---
title: macro Max (Minwindef. h)
description: A macro Max compara dois valores e retorna o maior. O tipo de dados pode ser qualquer tipo de dados numéricos, assinados ou não assinados. O tipo de dados dos argumentos e o valor de retorno são os mesmos.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- Multimídia máxima do Windows de macro
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
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499326"
---
# <a name="max-macro"></a>macro máx

A macro **Max** compara dois valores e retorna o maior. O tipo de dados pode ser qualquer tipo de dados numéricos, assinados ou não assinados. O tipo de dados dos argumentos e o valor de retorno são os mesmos.

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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o maior dos dois valores especificados.

## <a name="remarks"></a>Comentários

A macro **Max** é definida da seguinte maneira:


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





