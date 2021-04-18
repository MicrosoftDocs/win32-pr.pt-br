---
description: O método fechamento manipula mensagens de fechamento do WM \_ .
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Método CBaseWindow. fechamento (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751899"
---
# <a name="cbasewindowonclose-method"></a>Método CBaseWindow. fechamento

O `OnClose` método manipula mensagens de fechamento do WM \_ .

## <a name="syntax"></a>Sintaxe


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna **true**.

## <a name="remarks"></a>Comentários

Na classe base, esse método simplesmente oculta a janela. Normalmente, uma classe derivada substituirá esse método para que ele envie um evento [**EC \_ userabort**](ec-userabort.md) também. Não substitua o método para destruir a janela. Em vez disso, chame o método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) quando o filtro proprietário for destruído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




