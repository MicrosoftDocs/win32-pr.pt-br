---
description: Ocorre quando o controle InkPicture conclui a redesenho de si mesmo.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture. pintado (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772557"
---
# <a name="inkpicturepainted-event"></a>Evento InkPicture. pintado

Ocorre quando o controle [InkPicture](inkpicture-control-reference.md) conclui a redesenho de si mesmo.

## <a name="syntax"></a>Sintaxe


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HDC* \[ no\]
</dt> <dd>

O contexto do dispositivo no qual o evento ocorreu.

</dd> <dt>

*Rect* \[ no\]
</dt> <dd>

O [**InkRectangle**](inkrectangle-class.md) que foi redesenhado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nos dispinterfaces **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** com uma ID de \_ IOEPainted DISPID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




