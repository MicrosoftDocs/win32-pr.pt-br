---
description: O método GetDisplayFormat recupera um formato de vídeo que descreve o modo de exibição atual.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Método CImageDisplay. GetDisplayFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8841e95f4097d043e7ef01abdb067c248f43b9295a8c8466ba50f07d23bd7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074140"
---
# <a name="cimagedisplaygetdisplayformat-method"></a>Método CImageDisplay. GetDisplayFormat

O `GetDisplayFormat` método recupera um formato de vídeo que descreve o modo de exibição atual.

## <a name="syntax"></a>Sintaxe


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




