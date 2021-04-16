---
description: O método SetTemporalCompression especifica se os exemplos são compactados usando a compactação temporal (entre quadros).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Método CMediaType. SetTemporalCompression (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754261"
---
# <a name="cmediatypesettemporalcompression-method"></a>Método CMediaType. SetTemporalCompression

O `SetTemporalCompression` método especifica se os exemplos são compactados usando a compactação temporal (entre quadros).

## <a name="syntax"></a>Sintaxe


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bCompressed* 
</dt> <dd>

Valor booliano que especifica se o fluxo usa compactação temporal. Se o fluxo usar a compactação temporal, defina o valor como **true**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método define o membro **bTemporalCompression** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




