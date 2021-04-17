---
description: O método InitialiseWindow Inicializa a janela.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Inimétodo tialiseWindow (Winutil. h)
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
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812853"
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

*HWND* 
</dt> <dd>

Identificador para a janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Por padrão, esse método recupera um identificador para o contexto de dispositivo (DC) da janela e cria um controlador de domínio de memória compatível. No entanto, se o valor do sinalizador [**CBaseWindow:: m \_ BDoGetDC**](cbasewindow-m-bdogetdc.md) for **false**, esse método não recuperará os contextos do dispositivo. O DC de memória é útil para selecionar bitmaps antes de blittable para a janela.

O método [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




