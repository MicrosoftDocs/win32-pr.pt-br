---
description: Construtor de CMediaSample. CMediaSample-método de construtor.
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
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095434"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




