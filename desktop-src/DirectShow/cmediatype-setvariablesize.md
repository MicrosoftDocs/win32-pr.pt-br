---
description: O método setvariableize especifica que os exemplos não têm um tamanho fixo.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Método CMediaType. setvariableize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 118167d0068c058c925e5b63e2e951ff860917c40a5c3533daf9f02e6927649a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073960"
---
# <a name="cmediatypesetvariablesize-method"></a>Método CMediaType. setvariableize

O `SetVariableSize` método especifica que os exemplos não têm um tamanho fixo.

## <a name="syntax"></a>Sintaxe


```C++
void SetVariableSize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método define o membro **bFixedSizeSamples** como **false**. As chamadas subsequentes para o método [**CMediaType:: Getsampleize**](cmediatype-getsamplesize.md) retornam zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




