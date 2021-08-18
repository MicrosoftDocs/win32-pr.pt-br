---
description: Construtor CMediaSample.CMediaSample – Método do construtor.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Construtor CMediaSample.CMediaSample (Amfilter.h)
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
ms.openlocfilehash: 5baa5b791078eaf292b8da89fe50adaf7de9172185f8e6cab8745781030f401f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634686"
---
# <a name="cmediasamplecmediasample-constructor"></a>Construtor CMediaSample.CMediaSample

Método do construtor.

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

*Pname* 
</dt> <dd>

Ignorado.

</dd> <dt>

*pAllocator* 
</dt> <dd>

Ponteiro para o [**objeto CBaseAllocator**](cbaseallocator.md) que criou este exemplo.

</dd> <dt>

*Phr* 
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

A classe base não modifica o **valor HRESULT** passado no *parâmetro phr.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




