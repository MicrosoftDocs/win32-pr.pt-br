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
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787429"
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

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro retorna E \_ NOTIMPL por padrão. Isso informa ao distribuidor de plug-in do [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) que esse processador não implementa um processador de tela inteira.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




