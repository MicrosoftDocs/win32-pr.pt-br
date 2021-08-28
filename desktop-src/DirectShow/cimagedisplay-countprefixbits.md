---
description: O método CountPrefixBits calcula o número de zero bits no início de um campo de bits especificado.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Método CImageDisplay.CountPrefixBits (Winutil.h)
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
ms.openlocfilehash: 510ac01baab55fbf45e3441296018426335a8f50061f06400872fd7275d3e273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108476"
---
# <a name="cimagedisplaycountprefixbits-method"></a>Método CImageDisplay.CountPrefixBits

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

Especifica um campo de bits como um **valor DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de zero bits que ocorrem antes do primeiro 1 bit ou 0x80000000 se todos os bits são zero.

## <a name="remarks"></a>Comentários

Esse método é útil para trabalhar com máscaras de cores em [**estruturas VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




