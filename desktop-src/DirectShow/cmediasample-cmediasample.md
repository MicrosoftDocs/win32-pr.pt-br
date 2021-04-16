---
description: Método de construtor.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Construtor CMediaSample. CMediaSample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775635"
---
# <a name="cmediasamplecmediasample-constructor"></a>Construtor CMediaSample. CMediaSample

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ignorado.

</dd> <dt>

*pAllocator* 
</dt> <dd>

Ponteiro para o objeto [**CBaseAllocator**](cbaseallocator.md) que criou este exemplo.

</dd> <dt>

*phr* 
</dt> <dd>

Ignorado.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Ponteiro para um buffer de memória alocado pelo chamador, de tamanho *.*

</dd> <dt>

*length* 
</dt> <dd>

Comprimento do buffer de memória.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe base não modifica o valor **HRESULT** passado no parâmetro *PHR* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




