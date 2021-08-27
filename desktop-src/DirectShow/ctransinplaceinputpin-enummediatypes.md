---
description: Método CTransInPlaceInputPin.EnumMediaTypes – o método EnumMediaTypes enumera os tipos de mídia preferenciais do pino. Esse método implementa o método IPin::EnumMediaTypes.
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Método CTransInPlaceInputPin.EnumMediaTypes (Transip.h)
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
ms.openlocfilehash: 7f0c60a3fd20887975011ba54fba374d0af880cb2711bb501a40d64c6a66f206
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076216"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a>Método CTransInPlaceInputPin.EnumMediaTypes

O `EnumMediaTypes` método enumera os tipos de mídia preferenciais do pino. Esse método implementa o [**método IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ppenum* 
</dt> <dd>

Recebe um ponteiro para a interface [**IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Memória insuficiente.<br/>             |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>             | **Ponteiro NULL.**<br/>                |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | O pino de saída não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método retorna a interface **IEnumMediaTypes** do pino de entrada downstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




