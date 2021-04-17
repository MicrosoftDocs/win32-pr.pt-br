---
description: O método GetRestorePosition recupera a posição para a qual a janela será restaurada quando ela não for maximizada ou minimizada.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Método CBaseControlWindow. GetRestorePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752724"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>Método CBaseControlWindow. GetRestorePosition

O `GetRestorePosition` método recupera a posição para a qual a janela será restaurada quando ela não for maximizada ou minimizada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRestorePosition(
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

Ponteiro para o valor da coordenada da extrema esquerda.

</dd> <dt>

*pTop* 
</dt> <dd>

Ponteiro para o valor da parte superior da janela.

</dd> <dt>

*pWidth* 
</dt> <dd>

Ponteiro para o valor da largura da janela.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para o valor da altura da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Isso é o mesmo que os valores retornados pela função [**CBaseControlWindow:: GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) quando a janela não é maximizada nem minimizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




