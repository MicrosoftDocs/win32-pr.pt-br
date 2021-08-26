---
description: O método GetWindowPosition recupera as coordenadas atuais da janela.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Método CBaseControlWindow.GetWindowPosition (Ctlutil.h)
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
ms.openlocfilehash: 6d576f065e807c2af47621d43940d7e48c54f36f0617d20590953a5e83ab2fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966726"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>Método CBaseControlWindow.GetWindowPosition

O `GetWindowPosition` método recupera as coordenadas atuais da janela.

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

Ponteiro para a coordenada esquerda, em coordenadas de tela.

</dd> <dt>

*pTop* 
</dt> <dd>

Ponteiro para a coordenada superior, em coordenadas de tela.

</dd> <dt>

*Pwidth* 
</dt> <dd>

Ponteiro para a largura da janela, em coordenadas de tela.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para a altura da janela, em coordenadas de tela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




