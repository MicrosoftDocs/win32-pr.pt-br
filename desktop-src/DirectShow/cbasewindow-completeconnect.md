---
description: O método CompleteConnect notifica a janela de que o pino de entrada do renderizador foi conectado.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Método CBaseWindow. CompleteConnect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770106"
---
# <a name="cbasewindowcompleteconnect-method"></a>Método CBaseWindow. CompleteConnect

O `CompleteConnect` método notifica a janela que o pino de entrada do renderizador foi conectado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método redefine o sinalizador de ativação da janela ([**CBaseWindow:: m \_ bActivated**](cbasewindow-m-bactivated.md)) como **false**. Quando um processador de vídeo conclui uma conexão de PIN, ele pode chamar o método [**CBaseWindow:: ActivateWindow**](cbasewindow-activatewindow.md) para definir o tamanho e a posição da janela. Para forçar o **ActivateWindow** a recalcular esses atributos, primeiro chame o `CompleteConnect` método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




