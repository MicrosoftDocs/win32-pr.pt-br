---
description: O método Get recupera o item na posição especificada.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Método CGenericList.Get (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dae90872ea607571b215aafe3f9f35a645cd50d140dcbad0783369ce2189c881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813766"
---
# <a name="cgenericlistget-method"></a>Método CGenericList.Get

O `Get` método recupera o item na posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Indicador de posição para o item a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para um objeto do tipo **OBJECT** (o tipo de modelo).

## <a name="remarks"></a>Comentários

Se *pos* for **NULL,** o método retornará **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




