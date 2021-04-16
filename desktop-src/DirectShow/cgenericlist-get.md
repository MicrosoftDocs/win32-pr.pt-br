---
description: O método Get recupera o item na posição especificada.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Método CGenericList. Get (Wxlist. h)
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
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750481"
---
# <a name="cgenericlistget-method"></a>Método CGenericList. Get

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

Indicador de posição do item a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo).

## <a name="remarks"></a>Comentários

Se o *PDV* for **nulo**, o método retornará **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




