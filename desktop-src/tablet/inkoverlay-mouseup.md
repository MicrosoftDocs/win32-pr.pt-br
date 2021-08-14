---
description: Evento InkOverlay.MouseUp – ocorre quando o ponteiro do mouse está sobre o objeto InkCollector ou InkOverlay e um botão do mouse é liberado.
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: Evento InkOverlay.MouseUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 675c588d12976a506afec02e1bec58d97a99fd13ec897250f0e472dfbc519490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219782"
---
# <a name="inkoverlaymouseup-event"></a>Evento InkOverlay.MouseUp

Ocorre quando o ponteiro do mouse está sobre o [**objeto InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) e um botão do mouse é liberado.

## <a name="syntax"></a>Sintaxe


```C++
void MouseUp(
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

O botão do mouse que foi liberado.

</dd> <dt>

*Shift* \[ Em\]
</dt> <dd>

O estado da tecla SHIFT.

</dd> <dt>

*pX* \[ Em\]
</dt> <dd>

A coordenada X, em pixels, de um clique do mouse.

</dd> <dt>

*pY* \[ Em\]
</dt> <dd>

A coordenada y, em pixels, de um clique do mouse.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Se o evento deve ser cancelado para o controle pai. O valor padrão é **FALSE,** que especifica que o evento não deve ser cancelado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para melhorar o desempenho de tinta em tempo real, o oculta ou mostra o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)

> [!Note]  
> As propriedades *pX* e *pY* estão em pixels e não nas unidades HIMETRIC associadas ao espaço de tinta. Isso ocorre porque esse evento substitui o evento do mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas pixels.

 

> [!Note]  
> Alguns controles dependem de uma relação específica entre os [**eventos MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp.**](inkcollector-mouseup.md) Cancelar alguns desses eventos pode ter resultados imprevistos.

 

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de \_ DISPID IPEMouseUp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Enumeração InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




