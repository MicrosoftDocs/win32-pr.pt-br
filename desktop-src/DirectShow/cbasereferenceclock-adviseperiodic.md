---
description: 'O método AdvisePeriodic cria uma solicitação de aviso periódica. Esse método implementa o método IReferenceClock:: AdvisePeriodic.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Método CBaseReferenceClock. AdvisePeriodic (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754999"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>Método CBaseReferenceClock. AdvisePeriodic

O `AdvisePeriodic` método cria uma solicitação de aviso periódica. Esse método implementa o método [**IReferenceClock:: AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartTime* 
</dt> <dd>

Hora da primeira notificação, em unidades de 100 a nanossegundos. Deve ser maior que zero e menor que o \_ tempo máximo.

</dd> <dt>

*Período de tempo* 
</dt> <dd>

Tempo entre notificações, em unidades de 100 a nanossegundos. Deve ser maior que zero.

</dd> <dt>

*hSemaphore* 
</dt> <dd>

Identificador para um semáforo, criado pelo chamador.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Ponteiro para uma variável que recebe um identificador para a solicitação de aviso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Sucesso<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valores de tempo inválidos<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Falha<br/>                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Argumento de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

Em cada hora de notificação, o relógio libera o semáforo especificado no parâmetro *hSemaphore* . Quando nenhuma notificação adicional for necessária, chame o método [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) e passe o valor de *pdwAdviseToken* retornado dessa chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




