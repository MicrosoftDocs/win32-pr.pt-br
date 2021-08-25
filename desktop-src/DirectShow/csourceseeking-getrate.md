---
description: 'Método CSourceSeeking. GetRate – o método GetRate recupera a taxa de reprodução. Esse método implementa o método IMediaSeeking:: GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Método CSourceSeeking. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b734a5fafba9e38abbe853a8f3592a212130bf9a68de0efe7125aeea0ea01b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083946"
---
# <a name="csourceseekinggetrate-method"></a>Método CSourceSeeking. GetRate

O `GetRate` método recupera a taxa de reprodução. Esse método implementa o método [**IMediaSeeking:: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdRate* 
</dt> <dd>

Ponteiro para uma variável que recebe a taxa de reprodução.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Valor de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

A taxa de reprodução é especificada pela variável de membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




