---
description: O método CheckBitFields valida as máscaras de cor em uma estrutura VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Método CImageDisplay.CheckBitFields (Winutil.h)
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
ms.openlocfilehash: 44e60b6693dde202cd458cd09495dce9e4bea52ed96a468a8d3dcb6b2370eac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074170"
---
# <a name="cimagedisplaycheckbitfields-method"></a>Método CImageDisplay.CheckBitFields

O `CheckBitFields` método valida as máscaras de cor em uma estrutura [**VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

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

Ponteiro para uma **estrutura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se as máscaras de cor são válidas ou **FALSE** caso contrário.

## <a name="remarks"></a>Comentários

Esse método verifica se a máscara de cor para cada componente de cor tem entre um e oito bits e se cada máscara de cor é uma sequência contígua de bits. Chame esse método somente quando o **membro biCompression** estiver definido como BI \_ BITFIELDS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




