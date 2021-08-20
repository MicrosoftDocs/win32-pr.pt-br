---
description: Ocorre quando o ponteiro do mouse está sobre o controle InkPicture e um botão do mouse é pressionado.
ms.assetid: ff776b2b-7dd8-4d3d-b0f6-714b186d447e
title: Evento InkPicture.MouseDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bd844d4666f3ff0e1ca22e233a13cc09cdcd0b1090634b934dfc3ee9ee8a288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042078"
---
# <a name="inkpicturemousedown-event"></a>Evento InkPicture.MouseDown

Ocorre quando o ponteiro do mouse está sobre o [controle InkPicture](inkpicture-control-reference.md) e um botão do mouse é pressionado.

## <a name="syntax"></a>Sintaxe


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Botão* \[ Em\]
</dt> <dd>

O botão que foi pressionado.

</dd> <dt>

*Shift* \[ Em\]
</dt> <dd>

O estado da tecla SHIFT.

</dd> <dt>

*pX* \[ Em\]
</dt> <dd>

A coordenada X, em pixels, do [**objeto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*pY* \[ Em\]
</dt> <dd>

A coordenada y, em pixels, do [**objeto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar esse evento para o controle pai; caso contrário, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Os parâmetros pX e pY estão em pixels e não nas unidades HIMETRIC associadas ao sistema de coordenadas de espaço de tinta. Isso ocorre porque esse evento substitui o evento do mouse relacionado de um aplicativo que não tem reconhecimento de caneta e esse tipo de aplicativo se refere apenas a pixels.

 

> [!Caution]  
> Alguns controles dependem de uma relação específica entre os **eventos MouseDown,** [**MouseMove**](inkpicture-mousemove.md)e [**MouseUp.**](inkpicture-mouseup.md) Cancelar alguns desses eventos pode ter resultados imprevistos.

 

Esse método de evento é definido na interface **\_ IInkPictureEvents.** A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador dispID \_ IPEMouseDown.

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

 

