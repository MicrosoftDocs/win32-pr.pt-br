---
description: Esse operador testa a igualdade entre os objetos CMediaType.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'CMediaType. CMediaType:: Operator = = método (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784032"
---
# <a name="cmediatypecmediatypeoperator-method"></a>Método CMediaType. CMediaType:: Operator = =

Esse operador testa a igualdade entre os objetos [**CMediaType**](cmediatype.md) .

## <a name="syntax"></a>Sintaxe


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RT* \[ referência\]
</dt> <dd>

Referência ao objeto **CMediaType** a ser comparado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se *RT* for igual a este objeto. Caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




