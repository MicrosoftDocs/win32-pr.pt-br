---
description: O método CompleteConnect notifica a janela de que o pino de entrada do renderdor foi conectado.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Método CBaseWindow.CompleteConnect (Winutil.h)
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
ms.openlocfilehash: 5e04e0adf1d11a4878d860dd5c8a1eea9395095c71d8b5c86d6023a24ccdb28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016704"
---
# <a name="cbasewindowcompleteconnect-method"></a>Método CBaseWindow.CompleteConnect

O `CompleteConnect` método notifica a janela de que o pino de entrada do renderista foi conectado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método redefine o sinalizador de ativação da janela ([**CBaseWindow::m \_ bActivated**](cbasewindow-m-bactivated.md)) para **FALSE.** Quando um renderador de vídeo conclui uma conexão de pino, ele pode chamar o método [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) para definir o tamanho e a posição da janela. Para forçar **o ActivateWindow** a recalcular esses atributos, primeiro chame o `CompleteConnect` método .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




