---
description: O método CountSetBits retorna o número de bits definido como 1 em um campo de bit especificado.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Método CImageDisplay. CountSetBits (Winutil. h)
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
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810252"
---
# <a name="cimagedisplaycountsetbits-method"></a>Método CImageDisplay. CountSetBits

O `CountSetBits` método retorna o número de bits definido como 1 em um campo de bit especificado.

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

Especifica um campo de bits como um valor **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de bits que são definidos como 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




