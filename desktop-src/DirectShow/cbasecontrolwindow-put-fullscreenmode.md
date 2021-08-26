---
description: O \_ método Put fullscreenmode define o modo de tela inteira do processador.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Método de CBaseControlWindow.put_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e7aa121ce78198fe6b2ca0b88109183665f0cd93dd95294a848a2b2d0c03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983676"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>CBaseControlWindow. put \_ método fullscreenmode

O `put_FullScreenMode` método define o modo de tela inteira do processador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tela inteira* 
</dt> <dd>

Modo de tela inteira a ser aplicado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . A implementação atual retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Um processador de vídeo que implementa um modo de tela inteira deve substituir essa função de membro e implementar quaisquer modos com suporte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




