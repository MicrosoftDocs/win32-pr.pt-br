---
description: O método CheckHeaderValidity valida uma estrutura BITMAPINFOHEADER. Esse método é útil apenas para tipos RGB descompactados, não para tipos compactados ou tipos YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Método CImageDisplay.CheckHeaderValidity (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c8ce12f7e383e04942184e3897d0ddc52700a1a621844719d94f54f60203ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652356"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>Método CImageDisplay.CheckHeaderValidity

O `CheckHeaderValidity` método valida uma estrutura [**BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Esse método é útil apenas para tipos RGB descompactados, não para tipos compactados ou tipos YUV.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInput* 
</dt> <dd>

Ponteiro para uma [**estrutura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que contém a **estrutura BITMAPINFOHEADER.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o **BITMAPINFOHEADER for** válido ou **FALSE** caso contrário.

## <a name="remarks"></a>Comentários

Esse método verifica se as dimensões da imagem não são negativas; o tipo de compactação é BI RGB ou BI BITFIELDS; a profundidade da cor e as máscaras de cor são válidas; o membro biPlanes é igual a um; e os membros \_ \_ **biSize** e **biSizeImage**  estão corretos. Ele também verifica se há erros comuns nas entradas da paleta, se há.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




