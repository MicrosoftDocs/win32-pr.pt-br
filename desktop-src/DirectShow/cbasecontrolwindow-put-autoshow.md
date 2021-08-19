---
description: O método put \_ AutoShow define o sinalizador de estado AutoShow.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: CBaseControlWindow.put_AutoShow método (Ctlutil.h)
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
ms.openlocfilehash: a8e24686baa3cf1f2ad570394acd7a290ac374043b8564566dc1e89668d3f6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017274"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>Método CBaseControlWindow.put \_ AutoShow

O `put_AutoShow` método define o sinalizador de estado AutoShow.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Autoshow* 
</dt> <dd>

Sinalizador booliana de automação (0 está desligado, 1 está on).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa propriedade simplifica o acesso de exibição de janela para aplicativos. Se isso for definido como 1 (ativado), a janela, que normalmente fica oculta após o filtro ser conectado, será exibida automaticamente quando o filtro pausar ou for executado. No entanto, a janela não deve ser ocultada quando o filtro é interrompido. Se estiver definido como 0 (desligado), a janela será visível somente quando o aplicativo chamar [**CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) com os parâmetros apropriados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




