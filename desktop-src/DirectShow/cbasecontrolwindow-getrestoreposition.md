---
description: O método GetRestorePosition recupera a posição na qual a janela será restaurada quando não for maximizada ou minimizada.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Método CBaseControlWindow.GetRestorePosition (Ctlutil.h)
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
ms.openlocfilehash: 215b71d731227641df02716dd2b760f7e023bbec0c50bc66ac6d390ed87d002e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757606"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>Método CBaseControlWindow.GetRestorePosition

O `GetRestorePosition` método recupera a posição na qual a janela será restaurada quando não for maximizada ou minimizada.

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

Ponteiro para o valor da coordenada mais à esquerda.

</dd> <dt>

*pTop* 
</dt> <dd>

Ponteiro para o valor da parte superior da janela.

</dd> <dt>

*Pwidth* 
</dt> <dd>

Ponteiro para o valor da largura da janela.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para o valor da altura da janela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Isso é o mesmo que os valores retornados pela função [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) quando a janela não é maximizada nem minimizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




