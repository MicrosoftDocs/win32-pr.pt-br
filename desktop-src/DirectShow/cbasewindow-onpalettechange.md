---
description: O método OnPaletteChange lida com mensagens de alteração de paleta.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Método CBaseWindow.OnPaletteChange (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c881c519706ca0288847a7dc603cf513a99cdd76e4c83f0e53bec16df840e509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657949"
---
# <a name="cbasewindowonpalettechange-method"></a>Método CBaseWindow.OnPaletteChange

O `OnPaletteChange` método lida com mensagens de alteração de paleta.

## <a name="syntax"></a>Sintaxe


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador da janela.

</dd> <dt>

*Message* 
</dt> <dd>

Identificador de mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 0 se a mensagem tiver sido processada ou 1 se a mensagem não tiver sido processada.

## <a name="remarks"></a>Comentários

Esse método lida com mensagens WM \_ PALETTECHANGED e WM \_ QUERYNEWPALETTE. Ele chama o [**método CBaseWindow::D oRealisePalette**](cbasewindow-dorealisepalette.md) para realizar a nova paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




