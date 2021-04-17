---
description: O método CheckHeaderValidity valida uma estrutura BITMAPINFOHEADER. Esse método é útil apenas para tipos RGB não compactados, não para tipos não compactados ou tipos YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Método CImageDisplay. CheckHeaderValidity (Winutil. h)
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
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770098"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>Método CImageDisplay. CheckHeaderValidity

O `CheckHeaderValidity` método valida uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Esse método é útil apenas para tipos RGB não compactados, não para tipos não compactados ou tipos YUV.

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

Ponteiro para uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que contém a estrutura **BITMAPINFOHEADER** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se **BITMAPINFOHEADER** for válido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esse método verifica se as dimensões da imagem são não negativas; o tipo de compactação é BI \_ RGB ou bi \_ BITFIELDS; a profundidade de cor e as máscaras de cor são válidas; o membro **Biplans** é igual a um; e os membros **biSize** e **biSizeImage** estão corretos. Ele também verifica erros comuns nas entradas da paleta, se houver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




