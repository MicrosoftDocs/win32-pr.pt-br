---
description: O método InitialiseWindow inicializa a janela.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Inimétodo tialiseWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f260f60111f715bfce357e264b65bb4b821c5ca890d39d4d54e7269a191df303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954655"
---
# <a name="cbasewindowinitialisewindow-method"></a>CBaseWindow.Inimétodo tialiseWindow

O `InitialiseWindow` método inicializa a janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Por padrão, esse método recupera um handle para o DC (contexto de dispositivo) da janela e cria um DC de memória compatível. Se o valor do [**sinalizador CBaseWindow::m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md) for **FALSE,** no entanto, esse método não recuperará os contextos do dispositivo. O DC de memória é útil para selecionar bitmaps antes de blitá-los na janela.

O [**método CBaseWindow::D oCreateWindow**](cbasewindow-docreatewindow.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




