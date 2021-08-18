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
ms.openlocfilehash: 4769aff01c251017734fd7152fa703cd51064db11fb91851fd0b8fed76fc3d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635696"
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

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro usa os mesmos parâmetros que a função Microsoft Win32 **userwindow** (por exemplo, WS- \_ normal, WS \_ SHOWMINNOACTIVATE e WS não \_ Maximized).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




