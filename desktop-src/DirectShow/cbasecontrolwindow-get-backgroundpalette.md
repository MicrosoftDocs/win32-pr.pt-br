---
description: O \_ método Get BackgroundPalette recupera a paleta realizada no sinalizador de segundo plano.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Método de CBaseControlWindow.get_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749644"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>CBaseControlWindow. obter \_ método BackgroundPalette

O `get_BackgroundPalette` método recupera a paleta realizada no sinalizador de segundo plano.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBackgroundPalette* 
</dt> <dd>

Ponteiro para um sinalizador booliano de automação (0 está desativado, 1 está ativado).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IVideoWindow:: get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) . Se um vídeo for reproduzido dentro de outro aplicativo ou documento, talvez o aplicativo queira usar sua própria paleta. Ele pode perguntar se o vídeo usa a paleta de primeiro plano atual em vez de sua própria definindo esse sinalizador como 1. Se isso for definido como 0, a janela será instalada e perceberá sua própria paleta preferida. Observe que solicitar que a janela use uma paleta diferente causará severas penalidades de desempenho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




