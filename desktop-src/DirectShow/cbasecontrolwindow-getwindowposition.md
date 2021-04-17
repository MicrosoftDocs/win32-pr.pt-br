---
description: O método GetWindowPosition recupera as coordenadas atuais para a janela.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Método CBaseControlWindow. GetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751280"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>Método CBaseControlWindow. GetWindowPosition

O `GetWindowPosition` método recupera as coordenadas atuais para a janela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pLeft* 
</dt> <dd>

Ponteiro para a coordenada esquerda, em coordenadas da tela.

</dd> <dt>

*pTop* 
</dt> <dd>

Ponteiro para a coordenada superior, em coordenadas da tela.

</dd> <dt>

*pWidth* 
</dt> <dd>

Ponteiro para a largura da janela, em coordenadas da tela.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para a altura da janela, em coordenadas da tela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




