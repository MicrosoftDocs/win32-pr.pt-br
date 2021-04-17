---
description: 'O método Aconselhetime cria uma solicitação de aviso de uma amostra. Esse método implementa o método IReferenceClock:: Aconselhetime.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Método CBaseReferenceClock. AdviseTime (Refclock. h)
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
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749029"
---
# <a name="cbasereferenceclockadvisetime-method"></a>Método CBaseReferenceClock. AdviseTime

O `AdviseTime` método cria uma solicitação de aviso de uma imagem. Esse método implementa o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .

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

Tempo de referência base, em unidades de 100 a nanossegundos.

</dd> <dt>

*fluxo de transmissão* 
</dt> <dd>

Tempo de deslocamento de fluxo, em unidades de 100 a nanossegundos.

</dd> <dt>

*hEvent* 
</dt> <dd>

Identificador para um evento, criado pelo chamador.

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

Esse método cria uma solicitação de aviso de uma imagem para o tempo de referência de *baseTime*  +  *streamtime*. A soma deve ser maior que zero e menor que \_ o tempo máximo, ou o método retorna E \_ INVALIDARG. Na hora solicitada, o relógio sinaliza o evento especificado no parâmetro *hEvent* .

Para cancelar a notificação antes da hora ser atingida, chame o método [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) e passe o valor de *pdwAdviseToken* retornado dessa chamada. Depois que a notificação tiver ocorrido, o relógio a limpará automaticamente, portanto, não é necessário chamar **Unadvise**. No entanto, não é um erro fazer isso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




