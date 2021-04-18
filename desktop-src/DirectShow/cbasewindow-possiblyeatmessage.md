---
description: O método PossiblyEatMessage permite que uma classe derivada encaminhe mensagens para outra janela.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Método CBaseWindow. PossiblyEatMessage (Winutil. h)
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
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751694"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>Método CBaseWindow. PossiblyEatMessage

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

*uMsg* 
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

## <a name="return-value"></a>Retornar valor

Retorna **true** se a mensagem foi encaminhada ou **false** caso contrário. A classe base retorna **false**.

## <a name="remarks"></a>Comentários

Antes que o método [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) manipule uma mensagem, ele chama `PossiblyEatMessage` . Se `PossiblyEatMessage` retornar **true**, **OnReceiveMessage** ignorará a mensagem. Uma classe derivada pode substituir `PossiblyEatMessage` para que ela encaminhe algumas mensagens para uma janela do proprietário. Por exemplo, a classe [**CBaseControlWindow**](cbasecontrolwindow.md) , que deriva de **CBaseWindow**, encaminha mensagens de teclado e mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




