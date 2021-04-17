---
description: O \_ método Put AutoShow define o sinalizador de estado de AutoApresentação.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Método de CBaseControlWindow.put_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755619"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>Método de automostrar CBaseControlWindow. put \_

O `put_AutoShow` método define o sinalizador de estado de AutoShow.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Mostrar automostrações* 
</dt> <dd>

Sinalizador booliano de automação (0 está desativado, 1 está ativado).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa propriedade simplifica o acesso de exibição da janela para aplicativos. Se isso for definido como 1 (ativado), a janela, que normalmente é ocultada após o filtro ser conectado, será exibida automaticamente quando o filtro for pausado ou executado. No entanto, a janela não deve ser ocultada quando o filtro é interrompido. Se for definido como 0 (off), a janela ficará visível somente quando o aplicativo chamar [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) com os parâmetros apropriados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




