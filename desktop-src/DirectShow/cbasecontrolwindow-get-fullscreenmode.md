---
description: O \_ método Get fullscreenmode recupera o modo de tela inteira atual.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Método de CBaseControlWindow.get_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cebd74fd51551249c339100ac2dd3eda4a171cc316cca575f27f5194480978ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660529"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a>Método CBaseControlWindow. get \_ fullscreenmode

O `get_FullScreenMode` método recupera o modo de tela inteira atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tela inteira* 
</dt> <dd>

Ponteiro para o modo de tela inteira atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro retorna E \_ NOTIMPL por padrão. Isso informa ao distribuidor de plug-in do [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) que esse processador não implementa um processador de tela inteira.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




