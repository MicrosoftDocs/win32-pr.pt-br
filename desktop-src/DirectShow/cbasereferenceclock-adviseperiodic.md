---
description: O método AdvisePeriodic cria uma solicitação de consultoria periódica. Esse método implementa o método IReferenceClock::AdvisePeriodic.
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Método CBaseReferenceClock.AdvisePeriodic (Refclock.h)
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
ms.openlocfilehash: e4b81fc8dfc33cc2a6e5207e984de0c2e693b8c00b8f8d35949d0bb7150484bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052426"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>Método CBaseReferenceClock.AdvisePeriodic

O `AdvisePeriodic` método cria uma solicitação de consultoria periódica. Esse método implementa o [**método IReferenceClock::AdvisePeriodic.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic)

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

Hora da primeira notificação, em unidades de 100 nanossegundos. Deve ser maior que zero e menor que MAX \_ TIME.

</dd> <dt>

*PeriodTime* 
</dt> <dd>

Tempo entre notificações, em unidades de 100 nanossegundos. Deve ser maior que zero.

</dd> <dt>

*hSemaphore* 
</dt> <dd>

Lidar com um semáforo, criado pelo chamador.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Ponteiro para uma variável que recebe um identificador para a solicitação de consultoria.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valores de tempo inválidos<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Falha<br/>                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | **Argumento de** ponteiro NULL<br/> |



 

## <a name="remarks"></a>Comentários

A cada hora de notificação, o relógio libera o semáforo especificado no *parâmetro hSemaphore.* Quando nenhuma notificação adicional for necessária, chame o método [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) e passe o *valor pdwAdviseToken* retornado dessa chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




