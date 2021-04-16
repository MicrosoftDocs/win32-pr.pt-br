---
description: 'O método EnumMediaTypes enumera os tipos de mídia preferenciais do PIN. Esse método implementa o método IPin:: EnumMediaTypes.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Método CTransInPlaceInputPin. EnumMediaTypes (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa634fa695eb0007b49fc1c36c730c7fbde361b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752481"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a>Método CTransInPlaceInputPin. EnumMediaTypes

O `EnumMediaTypes` método enumera os tipos de mídia preferenciais do PIN. Esse método implementa o método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* 
</dt> <dd>

Recebe um ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Memória insuficiente.<br/>             |
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Ponteiro **nulo** .<br/>                |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O pino de saída não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método retorna a interface **IEnumMediaTypes** do pino de entrada downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




