---
description: O método docreatewindow cria a janela.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: CBaseWindow.DoCmétodo reateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751900"
---
# <a name="cbasewindowdocreatewindow-method"></a>CBaseWindow.DoCmétodo reateWindow

O `DoCreateWindow` método cria a janela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.

## <a name="remarks"></a>Comentários

O método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




