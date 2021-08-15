---
description: Evento InkOverlay. MouseMove-ocorre quando o ponteiro do mouse é movido sobre o objeto InkCollector ou InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Evento InkOverlay. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b4bec85062f1cf07edefd3f5712c43b12bdbe98b5773a962372bb00a186fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219802"
---
# <a name="inkoverlaymousemove-event"></a>Evento InkOverlay. MouseMove

Ocorre quando o ponteiro do mouse é movido sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Sintaxe


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Botão* \[ no\]
</dt> <dd>

O botão do mouse que foi pressionado.

</dd> <dt>

*Shift* \[ no\]
</dt> <dd>

O estado da tecla SHIFT.

</dd> <dt>

*PX* \[ no\]
</dt> <dd>

A coordenada x, em pixels, de um clique do mouse.

</dd> <dt>

*pY* \[ no\]
</dt> <dd>

A coordenada y, em pixels, de um clique do mouse.

</dd> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

Se o evento deve ser cancelado para o controle pai. O valor padrão é **false**, que especifica que o evento não deve ser cancelado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta. Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.

 

> [!Note]  
> Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) . Cancelar alguns desses eventos pode ter resultados imprevistos.

 

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseMove de DISPID \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Enumeração InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




