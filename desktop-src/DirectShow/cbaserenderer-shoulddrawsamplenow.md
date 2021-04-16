---
description: O método ShouldDrawSampleNow determina como um exemplo é agendado para renderização.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Método CBaseRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751499"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a>Método CBaseRenderer. ShouldDrawSampleNow

O `ShouldDrawSampleNow` método determina como um exemplo é agendado para renderização.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ShouldDrawSampleNow(
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

Ponteiro para uma variável que contém a hora de início da amostra.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de término da amostra.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ false. Se a classe derivada substituir esse método, retorne um dos valores mostrados na tabela a seguir.



| Código de retorno                                                                               | Descrição                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O exemplo deve ser renderizado imediatamente.<br/>                              |
| <dl> <dt>**\_falso**</dt> </dl>   | O exemplo deve ser agendado para renderização, com base nos carimbos de data/hora.<br/> |
| <dl> <dt>**Código de erro**</dt> </dl> | Não processar este exemplo.<br/>                                              |



 

## <a name="remarks"></a>Comentários

O método [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) chama esse método. Por padrão, os exemplos são sempre agendados para renderização com base em seus carimbos de data/hora. A classe derivada pode substituir esse método; por exemplo, para implementar o controle de qualidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




