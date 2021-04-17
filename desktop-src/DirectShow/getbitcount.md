---
description: A função GetBitCount retorna o número de bits por pixel usado por um subtipo de vídeo especificado. Esta função é válida somente para subtipos RGB não compactados.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Função GetBitCount (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789950"
---
# <a name="getbitcount-function"></a>Função GetBitCount

A `GetBitCount` função retorna o número de bits por pixel usado por um subtipo de vídeo especificado. Esta função é válida somente para subtipos RGB não compactados.

## <a name="syntax"></a>Sintaxe


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSubtype* 
</dt> <dd>

Ponteiro para um **GUID** de subtipo de vídeo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de bits por pixel para esse subtipo ou o valor **USHRT \_ Max** se o subtipo não for reconhecido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




