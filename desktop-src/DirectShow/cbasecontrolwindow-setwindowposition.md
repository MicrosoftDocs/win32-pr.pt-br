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
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752912"
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

*Mantida* 
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

 

 




