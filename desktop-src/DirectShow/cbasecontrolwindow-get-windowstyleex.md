---
description: O \_ método Get WindowStyleEx recupera os estilos de janela estendidos.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: Método de CBaseControlWindow.get_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 082b541c9f04122616f4f96548f1b1e58d940a6060fb4af1ac0fe51fa4887bb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331206"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a>CBaseControlWindow. obter \_ método WindowStyleEx

O `get_WindowStyleEx` método recupera os estilos de janela estendidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWindowStyleEx* 
</dt> <dd>

Ponteiro para estilos de janela estendidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro recupera os estilos de janela estendida. Ele chama a função de membro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




