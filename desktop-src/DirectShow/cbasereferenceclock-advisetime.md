---
description: O método AdviseTime cria uma solicitação de consultoria única. Esse método implementa o método IReferenceClock::AdviseTime.
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Método CBaseReferenceClock.AdviseTime (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e50b864a63cdd021d82c0a2a73f4f9c3acb68d1afb1f6a2dcd8d8d575966a5fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502786"
---
# <a name="cbasereferenceclockadvisetime-method"></a>Método CBaseReferenceClock.AdviseTime

O `AdviseTime` método cria uma solicitação de consultoria única. Esse método implementa o [**método IReferenceClock::AdviseTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*baseTime* 
</dt> <dd>

Tempo de referência base, em unidades de 100 nanossegundos.

</dd> <dt>

*streamTime* 
</dt> <dd>

Tempo de deslocamento de fluxo, em unidades de 100 nanossegundos.

</dd> <dt>

*Hevent* 
</dt> <dd>

Manipular para um evento, criado pelo chamador.

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

Esse método cria uma solicitação de consultoria única para a hora de referência *baseTime*  +  *streamTime*. A soma deve ser maior que zero e menor que MAX \_ TIME ou o método retorna E \_ INVALIDARG. No momento solicitado, o relógio sinaliza o evento especificado no *parâmetro hEvent.*

Para cancelar a notificação antes que a hora seja atingida, chame o método [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) e passe o *valor pdwAdviseToken* retornado dessa chamada. Depois que a notificação ocorreu, o relógio a limpa automaticamente, portanto, não é necessário **chamar Unadvise**. No entanto, não é um erro fazer isso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




