---
description: O método CheckBitFields valida as máscaras de cores em uma estrutura VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Método CImageDisplay. CheckBitFields (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748199"
---
# <a name="cimagedisplaycheckbitfields-method"></a>Método CImageDisplay. CheckBitFields

O `CheckBitFields` método valida as máscaras de cores em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInput* 
</dt> <dd>

Ponteiro para uma estrutura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se as máscaras de cor forem válidas ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esse método verifica se a máscara de cor de cada componente de cor está entre um e oito bits e se cada máscara de cor é uma sequência contígua de bits. Chame esse método somente quando o membro **bicompressão** estiver definido como bi \_ BITFIELDS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




