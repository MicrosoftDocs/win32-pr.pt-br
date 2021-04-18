---
description: O método getbitmasks recupera as máscaras de cores para um formato VIDEOINFO especificado.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Método CImageDisplay. getbitmasks (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752086"
---
# <a name="cimagedisplaygetbitmasks-method"></a>Método CImageDisplay. getbitmasks

O `GetBitMasks` método recupera as máscaras de cores para um formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado.

## <a name="syntax"></a>Sintaxe


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Ponteiro para a estrutura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma matriz de três valores **DWORD** .

## <a name="remarks"></a>Comentários

Se o membro de **bicompressão** for bi \_ BITFIELDS, o método retornará um ponteiro para as máscaras de cores que são fornecidas no membro **dwBitMasks** . Se o membro de **bicompressão** for bi \_ RGB, o método retornará as máscaras de cores que correspondem à profundidade de bits. Se o método falhar (por exemplo, a profundidade de bit é menor que 16), o método retornará a matriz {0,0,0} .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




