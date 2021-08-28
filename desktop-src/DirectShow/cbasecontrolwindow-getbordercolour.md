---
description: O método GetBorderColorr recupera a cor da borda da janela atual, m \_ BorderColorr.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Método CBaseControlWindow.GetBorderColorr (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b5b94e0fa58c95e74fd140c04710e8aaacef9402397fa475983c0e01e586528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017364"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>Método CBaseControlWindow.GetBorderColorr

O `GetBorderColour` método recupera a cor da borda da janela atual, m **\_ BorderColorr**.

## <a name="syntax"></a>Sintaxe


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a cor da borda.

## <a name="remarks"></a>Comentários

Um aplicativo pode definir um retângulo de destino para exibir o vídeo. Esse retângulo deve ser relativo à área do cliente para a janela. Se isso for feito (o padrão é sempre pintar toda a janela), haverá uma área que envolve o vídeo; ou seja, a borda. A cor da borda pode ser definida por meio da função de membro [**CBaseControlWindow::p ut \_ BorderColor.**](cbasecontrolwindow-put-bordercolor.md) Essa propriedade afeta a cor da borda. Use essa função membro em vez [**de CBaseControlWindow::get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), a menos que você esteja chamando isso externamente por meio do [**método IVideoWindow::get \_ BorderColor.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




