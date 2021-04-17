---
description: O \_ método Put janelastate define o estado da janela.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Método de CBaseControlWindow.put_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749854"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>Método WindowState de CBaseControlWindow. put \_

O `put_WindowState` método define o estado da janela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*WindowState* 
</dt> <dd>

Novo estado da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro usa os mesmos parâmetros que a função Microsoft Win32 **userwindow** (por exemplo, WS- \_ normal, WS \_ SHOWMINNOACTIVATE e WS não \_ Maximized).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




