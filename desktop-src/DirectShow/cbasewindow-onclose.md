---
description: O método OnClose lida com mensagens WM \_ CLOSE.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Método CBaseWindow.OnClose (Winutil.h)
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
ms.openlocfilehash: 880e82ca527972b5074ac290fda34ad1c7868a33cbbe1cad12885b56720cef99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635136"
---
# <a name="cbasewindowonclose-method"></a>Método CBaseWindow.OnClose

O `OnClose` método trata mensagens WM \_ CLOSE.

## <a name="syntax"></a>Sintaxe


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna **TRUE.**

## <a name="remarks"></a>Comentários

Na classe base, esse método simplesmente oculta a janela. Normalmente, uma classe derivada substituirá esse método para que ele também envie um evento [**\_ EC USERABORT.**](ec-userabort.md) Não substitua o método para destruir a janela. Em vez disso, [**chame o método CBaseWindow::D oneWithWindow**](cbasewindow-donewithwindow.md) quando o filtro de propriedade for destruído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




