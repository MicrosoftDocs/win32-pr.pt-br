---
description: O método \_ get WindowStyle recupera os estilos de janela padrão.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: CBaseControlWindow.get_WindowStyle método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9356b449adbb4ee760ec70990c4db0b6703c16e9d0970f2756bac23907b1bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660255"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a>Método CBaseControlWindow.get \_ WindowStyle

O `get_WindowStyle` método recupera os estilos de janela padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWindowStyle* 
</dt> <dd>

Ponteiro para estilos de janela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro retorna os estilos de janela padrão, como WS \_ CHILD e WS \_ VISIBLE. Ele chama a função de membro [**CBaseControlWindow::D oGetWindowStyle.**](cbasecontrolwindow-dogetwindowstyle.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




