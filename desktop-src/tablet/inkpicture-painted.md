---
description: Ocorre quando o controle InkPicture foi concluído redesenhando a si mesmo.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture.Painted (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201027ba2626cd3a3dd8d76a8794a1a5430785e0e1602633ee9f39ac36caa023
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451046"
---
# <a name="inkpicturepainted-event"></a>Evento InkPicture.Painted

Ocorre quando o [controle InkPicture](inkpicture-control-reference.md) foi concluído redesenhando a si mesmo.

## <a name="syntax"></a>Sintaxe


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDC* \[ Em\]
</dt> <dd>

O contexto do dispositivo no qual o evento ocorreu.

</dd> <dt>

*Rect* \[ Em\]
</dt> <dd>

O [**InkRectangle**](inkrectangle-class.md) que foi repintado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas dispinterfaces **\_ IInkOverlayEvents** **\_ e IInkPictureEvents** com uma ID de \_ DISPID IOEPink.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




