---
description: O método GetBorderColour recupera a cor de borda da janela atual, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Método CBaseControlWindow. GetBorderColour (Ctlutil. h)
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
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753757"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>Método CBaseControlWindow. GetBorderColour

O `GetBorderColour` método recupera a cor da borda da janela atual, **m \_ BorderColour**.

## <a name="syntax"></a>Sintaxe


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna a cor da borda.

## <a name="remarks"></a>Comentários

Um aplicativo pode definir um retângulo de destino para exibir o vídeo. Esse retângulo deve ser relativo à área do cliente para a janela. Se isso for feito (o padrão é sempre pintar toda a janela), há uma área que circunda o vídeo; ou seja, a borda. A cor da borda pode ser definida por meio da função de membro [**CBaseControlWindow::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) . Essa propriedade afeta a cor da borda. Use essa função de membro em vez de [**CBaseControlWindow:: get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), a menos que você esteja chamando isso externamente por meio do método [**IVideoWindow:: get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




