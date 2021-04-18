---
description: O método CountPrefixBits calcula o número de zero bits no início de um campo de bits especificado.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Método CImageDisplay. CountPrefixBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751687"
---
# <a name="cimagedisplaycountprefixbits-method"></a>Método CImageDisplay. CountPrefixBits

O `CountPrefixBits` método calcula o número de zero bits no início de um campo de bits especificado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD CountPrefixBits(
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

Retorna o número de zero bits que ocorrem antes do primeiro 1 bit ou 0x80000000 se todos os bits forem zero.

## <a name="remarks"></a>Comentários

Esse método é útil para trabalhar com máscaras de cores em estruturas [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




