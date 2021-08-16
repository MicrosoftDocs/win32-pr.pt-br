---
description: O método GetSampleTimes recupera os carimbos de data/hora de um exemplo.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Método CBaseRenderer. GetSampleTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d759cbcf2a9638b54e6194bcac7e7b24254c0d37987995d511fb4ffce85f1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954955"
---
# <a name="cbaserenderergetsampletimes-method"></a>Método CBaseRenderer. GetSampleTimes

O `GetSampleTimes` método recupera os carimbos de data/hora de um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de início.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de término.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                                    | Descrição                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                           | O exemplo deve ser renderizado imediatamente.<br/>                              |
| <dl> <dt>**\_falso**</dt> </dl>                        | O exemplo deve ser agendado para renderização, com base nos carimbos de data/hora.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>                         | Não processar este exemplo.<br/>                                              |
| <dl> <dt>**VFW \_ \_ hora de início E \_ \_ término após o \_ final**</dt> </dl> | Carimbo de data/hora inadequado: a hora de término é anterior à hora de início.<br/>            |



 

## <a name="remarks"></a>Comentários

O filtro chama esse método para determinar como ele deve lidar com um exemplo. Se o valor de retorno for S \_ OK, o filtro renderizará o exemplo imediatamente. Se o valor de retorno for S \_ false, o filtro agendará o exemplo para renderização, com base nos carimbos de data/hora. Se o valor de retorno for um código de erro, o filtro rejeitará o exemplo.

Esse método retornará S \_ OK se o exemplo não tiver carimbos de data/hora ou se o filtro não tiver um relógio de referência. Caso contrário, ele retorna o valor do método [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) . Na classe base, **ShouldDrawSampleNow** sempre retorna S \_ false. A classe derivada pode substituir esse comportamento. Por exemplo, se a classe derivada implementar o gerenciamento de controle de qualidade, ela poderá retornar E \_ falhar ao descartar um exemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




