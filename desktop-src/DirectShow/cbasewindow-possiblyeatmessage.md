---
description: O método PossiblyEatMessage permite que uma classe derivada encaminhe mensagens para outra janela.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Método CBaseWindow.PossiblyEatMessage (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851f46d14f949a49c9422256f9b2bda1ba314e5789773121387e89c011f7a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016454"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>Método CBaseWindow.PossiblyEatMessage

O `PossiblyEatMessage` método permite que uma classe derivada encaminhe mensagens para outra janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Umsg* 
</dt> <dd>

Identificador de mensagem.

</dd> <dt>

*wParam* 
</dt> <dd>

Primeiro parâmetro de mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parâmetro de mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a mensagem tiver sido encaminhada ou **FALSE** caso contrário. A classe base retorna **FALSE.**

## <a name="remarks"></a>Comentários

Antes de [**o método CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) manipular uma mensagem, ele chama `PossiblyEatMessage` . Se `PossiblyEatMessage` retornar **TRUE,** **OnReceiveMessage** ignorará a mensagem. Uma classe derivada pode substituir `PossiblyEatMessage` para que ela encaminhe algumas mensagens para uma janela de proprietário. Por exemplo, a [**classe CBaseControlWindow,**](cbasecontrolwindow.md) que deriva de **CBaseWindow,** encaminha mensagens do teclado e do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




