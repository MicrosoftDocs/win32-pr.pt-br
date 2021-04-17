---
description: O método PaintWindow faz com que a janela seja repintada.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Método CBaseWindow. PaintWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752707"
---
# <a name="cbasewindowpaintwindow-method"></a>Método CBaseWindow. PaintWindow

O `PaintWindow` método faz com que a janela seja repintada.

## <a name="syntax"></a>Sintaxe


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bErase* 
</dt> <dd>

Valor booliano que especifica se o plano de fundo é apagado. Se o valor for **true**, o plano de fundo será apagado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método gera uma mensagem de pintura do WM \_ invalidando a área inteira do cliente da janela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




