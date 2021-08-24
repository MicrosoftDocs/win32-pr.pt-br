---
description: O \_ método obter AutoShow recupera o sinalizador de estado atual do AutoShow.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Método de CBaseControlWindow.get_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a5c16e0b460d07255cae113194f672ca3dace6f46827ac613c9559370284beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158789"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>Método de automostrar CBaseControlWindow. get \_

O `get_AutoShow` método recupera o sinalizador de estado atual do AutoShow.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Mostrar automostrações* 
</dt> <dd>

Ponteiro para um sinalizador booliano de automação (0 está desativado, 1 está ativado).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método de [**\_ automostrar IVideoWindow:: Get**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) . Essa propriedade simplifica o acesso de exibição da janela para aplicativos. Se isso for definido como 1 (ativado), a janela, que normalmente é ocultada após a conexão do filtro, será exibida automaticamente quando o filtro for pausado ou executado. No entanto, a janela não deve ser ocultada quando o filtro é interrompido. Se esse parâmetro for definido como 0 (off), a janela ficará visível somente quando o aplicativo chamar [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) com os parâmetros apropriados.

Essa função de membro deve ser chamada por objetos externos por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e, portanto, bloqueia a seção crítica para sincronizar com o filtro associado. Chame a função de membro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) para recuperar essa propriedade se você não estiver chamando de um objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




