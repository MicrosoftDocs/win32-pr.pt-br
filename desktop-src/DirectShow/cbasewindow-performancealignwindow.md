---
description: O método PerformanceAlignWindow alinha a posição da janela aos limites DWORD, para desempenho máximo.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Método CBaseWindow.PerformanceAlignWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3c077b6cf00f61565124f3d79ad905f6d34a3d8da50d58396e2df1bd35b0d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016464"
---
# <a name="cbasewindowperformancealignwindow-method"></a>Método CBaseWindow.PerformanceAlignWindow

O `PerformanceAlignWindow` método alinha a posição da janela aos limites **DWORD,** para desempenho máximo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método alinha as bordas esquerda e superior da janela aos limites DWORD, o que pode melhorar o desempenho. Se a janela tiver um pai, o método retornará S \_ OK, mas executará o alinhamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




