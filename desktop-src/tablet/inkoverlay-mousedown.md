---
description: Evento InkOverlay. MouseDown-ocorre quando o ponteiro do mouse está sobre o objeto InkCollector ou InkOverlay e um botão do mouse é pressionado.
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: Evento InkOverlay. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff1e4bff715a6585ee607de766c809579f527aa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086814"
---
# <a name="inkoverlaymousedown-event"></a>Evento InkOverlay. MouseDown

Ocorre quando o ponteiro do mouse está sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) e um botão do mouse é pressionado.

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

A coordenada X, em pixels, de um clique do mouse.

</dd> <dt>

*pY* \[ no\]
</dt> <dd>

A coordenada Y, em pixels, de um clique do mouse.

</dd> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**. O valor padrão é **Variant \_ false**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para melhorar o desempenho de tinta em tempo real, oculte ou mostre o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp**](inkcollector-mouseup.md) .

> [!Note]  
> As propriedades pX e pY estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta. Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.

 

> [!Note]  
> Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) . Cancelar alguns desses eventos pode ter resultados imprevistos.

 

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseDown de DISPID \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Enumeração InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Evento MouseUp**](inkcollector-mouseup.md)
</dt> </dl>

 

 




