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
ms.openlocfilehash: 63ea3fa8ecbc6e644ccc5f4b1fac7a2fcd9c18270474f45dc08faa164f76cbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660771"
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

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IVideoWindow:: get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) . Se um vídeo for reproduzido dentro de outro aplicativo ou documento, talvez o aplicativo queira usar sua própria paleta. Ele pode perguntar se o vídeo usa a paleta de primeiro plano atual em vez de sua própria definindo esse sinalizador como 1. Se isso for definido como 0, a janela será instalada e perceberá sua própria paleta preferida. Observe que solicitar que a janela use uma paleta diferente causará severas penalidades de desempenho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




