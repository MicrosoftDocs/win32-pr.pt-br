---
description: Evento InkCollector. MouseMove – ocorre quando o ponteiro do mouse é movido sobre o objeto InkCollector ou InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Evento InkCollector. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3392f2022af39600cb24461b26d37e5d624f4cb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110154"
---
# <a name="inkcollectormousemove-event"></a>Evento InkCollector. MouseMove

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

**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta. Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.

 

> [!Note]  
> Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), **MouseMove** e [**MouseUp**](inkcollector-mouseup.md) . Cancelar alguns desses eventos pode ter resultados imprevistos.

 

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseMove de DISPID \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Enumeração InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




