---
description: Evento InkOverlay.MouseDown – ocorre quando o ponteiro do mouse está sobre o objeto InkCollector ou InkOverlay e um botão do mouse é pressionado.
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: Evento InkOverlay.MouseDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b0d605dd36f4cae410de2514542aa15818d4604e4484352c68dac54b40b1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219262"
---
# <a name="inkoverlaymousedown-event"></a>Evento InkOverlay.MouseDown

Ocorre quando o ponteiro do mouse está sobre o [**objeto InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) e um botão do mouse é pressionado.

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

O botão do mouse que foi pressionado.

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

A coordenada Y, em pixels, de um clique do mouse.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **VARIANT \_ FALSE.** O valor padrão é **VARIANT \_ FALSE**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para melhorar o desempenho de tinta em tempo real, o oculta ou mostra o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)

> [!Note]  
> As propriedades pX e pY estão em pixels e não nas unidades HIMETRIC associadas ao espaço de tinta. Isso ocorre porque esse evento substitui o evento do mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas pixels.

 

> [!Note]  
> Alguns controles dependem de uma relação específica entre os [**eventos MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp.**](inkcollector-mouseup.md) Cancelar alguns desses eventos pode ter resultados imprevistos.

 

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de \_ DISPID IPEMouseDown.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Enumeração InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Evento MouseUp**](inkcollector-mouseup.md)
</dt> </dl>

 

 




