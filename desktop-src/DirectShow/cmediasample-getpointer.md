---
description: 'O método getapontarr recupera um ponteiro de leitura/gravação para o buffer. Esse método implementa o método IMediaSample:: getapontarr.'
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Método CMediaSample. GetPointer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21a39fae4f243c0a4e7305573f1b06ee2f11766729ef4933124d059b20b3a14b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832266"
---
# <a name="cmediasamplegetpointer-method"></a>Método CMediaSample. GetPointer

O `GetPointer` método recupera um ponteiro de leitura/gravação para o buffer. Esse método implementa o método [**IMediaSample:: Getapontarr**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para o buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




