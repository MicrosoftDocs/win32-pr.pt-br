---
description: O método IsAutoShowEnabled recupera informações sobre se a janela de vídeo é exibida automaticamente quando o filtro de renderização é pausado ou executado.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Método CBaseControlWindow. IsAutoShowEnabled (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81f5190d3b0634c763703a3e13aa711f097641285f49c469dab6bad6ce0d9055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660225"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>Método CBaseControlWindow. IsAutoShowEnabled

O `IsAutoShowEnabled` método recupera informações sobre se a janela de vídeo aparece automaticamente quando o filtro de renderização é pausado ou executado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **true** se o membro **m \_ bAutoShow** for definido como 1 ou **false** se estiver definido como 0.

## <a name="remarks"></a>Comentários

Se o membro **m \_ bAutoShow** for definido como 1 em uma janela de vídeo oculta, a janela ficará visível quando o filtro for pausado ou executado. Se esse membro for definido como 0, a janela será exibida somente se você usar a função de membro [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow \_ ::p UT**](cbasecontrolwindow-put-windowstate.md) com os parâmetros apropriados.

Essa função de membro recupera a configuração de membro **m \_ bAutoShow** e tem o mesmo resultado que usar o método [**IVideoWindow:: get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




