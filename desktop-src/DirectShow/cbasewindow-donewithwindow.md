---
description: O método DoneWithWindow destrói a janela.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Método CBaseWindow. DoneWithWindow (Winutil. h)
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
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750057"
---
# <a name="cbasewindowdonewithwindow-method"></a>Método CBaseWindow. DoneWithWindow

O `DoneWithWindow` método destrói a janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Chame esse método do método destruidor do objeto derivado.

Se esse método for chamado do mesmo thread que criou a janela, o método executará as seguintes ações:

-   Chama o método [**CBaseWindow:: InactivateWindow**](cbasewindow-inactivatewindow.md) , que desativa a janela.
-   Chama o método [**CBaseWindow:: UninitialiseWindow**](cbasewindow-uninitialisewindow.md) , que libera os recursos usados pela janela.
-   Destrói a janela.

Se a chamada de thread `DoneWithWindow` não for o thread que criou a janela, o método enviará uma mensagem "Destroy" privada para a janela. Quando a janela recebe essa mensagem, ela chama a `DoneWithWindow` si mesma. (Se [**CBaseWindow:: m \_ BDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) for **true**, a janela postará a mensagem.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




