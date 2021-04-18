---
description: O método OnPaletteChange manipula as mensagens de alteração da paleta.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Método CBaseWindow. OnPaletteChange (Winutil. h)
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
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757707"
---
# <a name="cbasewindowonpalettechange-method"></a>Método CBaseWindow. OnPaletteChange

O `OnPaletteChange` método manipula as mensagens de alteração da paleta.

## <a name="syntax"></a>Sintaxe


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Identificador para a janela.

</dd> <dt>

*Message* 
</dt> <dd>

Identificador de mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará 0 se a mensagem tiver sido processada ou 1 se a mensagem não tiver sido processada.

## <a name="remarks"></a>Comentários

Esse método manipula \_ as mensagens do WM PaletteChanged e do WM \_ QUERYNEWPALETTE. Ele chama o método [**CBaseWindow::D orealisepalette**](cbasewindow-dorealisepalette.md) para obter a nova paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




