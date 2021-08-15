---
description: O método GetDeliveryBuffer recupera um exemplo de mídia que contém um buffer vazio.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Método CBaseOutputPin. GetDeliveryBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d118e21ea67932529c41b35595619c6e03b907718708ba285aa2a6578177f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823605"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>Método CBaseOutputPin. GetDeliveryBuffer

O `GetDeliveryBuffer` método recupera um exemplo de mídia que contém um buffer vazio.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSample* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do buffer.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Ponteiro para a hora de início do exemplo, ou **NULL**.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Ponteiro para a hora de término da amostra ou **NULL**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinação de bits bit a bit de sinalizadores com suporte na interface [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | Nenhum alocador disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método **IMemAllocator:: GetBuffer** no alocador e passa os parâmetros para esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




