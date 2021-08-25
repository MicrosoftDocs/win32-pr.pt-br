---
description: O método SetWindowPosition define a posição da janela na área de trabalho.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Método CBaseControlWindow. SetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2734c93d1a3d3d3ea29e037d1bf85baacd5358a69f08d1517012c3eb250ab8ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635455"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>Método CBaseControlWindow. SetWindowPosition

O `SetWindowPosition` método define a posição da janela na área de trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Left* 
</dt> <dd>

Nova coordenada esquerda.

</dd> <dt>

*Top* 
</dt> <dd>

Nova coordenada superior.

</dd> <dt>

*Largura* 
</dt> <dd>

Largura da janela.

</dd> <dt>

*Altura* 
</dt> <dd>

Altura da janela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




