---
description: O método CountSetBits retorna o número de bits definido como 1 em um campo de bits especificado.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Método CImageDisplay.CountSetBits (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d334111c18c2c94c79a8b49ed7c0601efabb2bd13922a68c292970d4d2c379bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824066"
---
# <a name="cimagedisplaycountsetbits-method"></a>Método CImageDisplay.CountSetBits

O `CountSetBits` método retorna o número de bits definido como 1 em um campo de bits especificado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Campo* 
</dt> <dd>

Especifica um campo de bits como um **valor DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de bits definidos como 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




