---
description: O método setamostrate especifica um tamanho de amostra fixo ou especifica que os exemplos têm um tamanho variável.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Método CMediaType. setsampleize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a29393ed4c9251d1e12895ad57a61f96bdc80bb05757ce72fc9485bb42a1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954405"
---
# <a name="cmediatypesetsamplesize-method"></a>Método CMediaType. setsampleize

O `SetSampleSize` método especifica um tamanho de amostra fixo ou especifica que os exemplos têm um tamanho variável.

## <a name="syntax"></a>Sintaxe


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sz* 
</dt> <dd>

Tamanho da amostra, em bytes ou zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o valor de *sz* for zero, o tipo de mídia usará tamanhos de amostra variáveis. Caso contrário, o tamanho da amostra será corrigido em *sz* bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




