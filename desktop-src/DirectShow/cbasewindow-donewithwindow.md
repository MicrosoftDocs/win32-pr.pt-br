---
description: O método DoneWithWindow destrói a janela.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Método CBaseWindow.DoneWithWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6871a42e1a08693a7daf691195b86cd5a41dd208295dc625a33e41083b53adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016664"
---
# <a name="cbasewindowdonewithwindow-method"></a>Método CBaseWindow.DoneWithWindow

O `DoneWithWindow` método destrói a janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Chame esse método do método destruidor do objeto derivado.

Se esse método for chamado do mesmo thread que criou a janela, o método executará as seguintes ações:

-   Chama o [**método CBaseWindow::InactivateWindow,**](cbasewindow-inactivatewindow.md) que desativa a janela.
-   Chama o [**método CBaseWindow::UninitialiseWindow,**](cbasewindow-uninitialisewindow.md) que libera os recursos usados pela janela.
-   Destrói a janela.

Se a chamada de thread não for o thread que criou a janela, o método enviará uma `DoneWithWindow` mensagem "destruir" privada para a janela. Quando a janela recebe essa mensagem, ela chama `DoneWithWindow` por conta própria. (Se [**CBaseWindow::m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) for **TRUE,** a janela postará a mensagem.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




