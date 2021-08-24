---
description: O método GetPaletteVersion recupera a versão atual da paleta.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Método CDrawImage. GetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14cc4df95507a0c28bd61ec6db405f01353f9228419d0da84c4fc9fc35ca6b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537286"
---
# <a name="cdrawimagegetpaletteversion-method"></a>Método CDrawImage. GetPaletteVersion

O `GetPaletteVersion` método recupera a versão atual da paleta.

## <a name="syntax"></a>Sintaxe


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o valor da variável de membro **m \_ PaletteVersion** .

## <a name="remarks"></a>Comentários

O valor retornado por esse método se aplica somente quando o alocador é um objeto [**CImageAllocator**](cimageallocator.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




