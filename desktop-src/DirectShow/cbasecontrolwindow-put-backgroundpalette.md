---
description: O \_ método Put BackgroundPalette define um sinalizador para obter a paleta em segundo plano.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Método de CBaseControlWindow.put_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750686"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a>Método CBaseControlWindow. put \_ BackgroundPalette

O `put_BackgroundPalette` método define um sinalizador para obter a paleta em segundo plano.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*BackgroundPalette* 
</dt> <dd>

Sinalizador booliano de automação (0 está desativado, 1 está ativado).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Para reproduzir um vídeo dentro de outro aplicativo ou documento, o aplicativo pode querer usar sua própria paleta. Ele pode perguntar se o vídeo usa a paleta de primeiro plano atual, em vez de sua própria, como a paleta de plano de fundo, definindo esse sinalizador como 1. Se isso for definido como 0, a janela será instalada e perceberá sua própria paleta preferida. Pedir que a janela use uma paleta diferente causará severas penalidades de desempenho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




