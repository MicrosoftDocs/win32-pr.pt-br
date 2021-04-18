---
description: O método PerformanceAlignWindow alinha a posição da janela aos limites DWORD, para o desempenho máximo.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Método CBaseWindow. PerformanceAlignWindow (Winutil. h)
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
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778508"
---
# <a name="cbasewindowperformancealignwindow-method"></a>Método CBaseWindow. PerformanceAlignWindow

O `PerformanceAlignWindow` método alinha a posição da janela com os limites **DWORD** , para o desempenho máximo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método alinha as bordas esquerda e superior da janela aos limites DWORD, o que pode melhorar o desempenho. Se a janela tiver um pai, o método retornará S \_ OK, mas executará o alinhamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




