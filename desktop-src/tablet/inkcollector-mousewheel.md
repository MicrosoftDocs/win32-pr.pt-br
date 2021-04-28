---
description: Evento InkCollector. MouseWheel – ocorre quando a roda do mouse se move enquanto o objeto InkCollector ou InkOverlay tem foco.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Evento InkCollector. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851a017af4bb71917c88e2194db86eec64218771
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110134"
---
# <a name="inkcollectormousewheel-event"></a>Evento InkCollector. MouseWheel

Ocorre quando a roda do mouse se move enquanto o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) tem foco.

## <a name="syntax"></a>Sintaxe


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
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

*Delta* \[ no\]
</dt> <dd>

Uma contagem assinada do número de tentativas que a roda do mouse gira. Um detentor é um ponto da roda do mouse.

</dd> <dt>

*x* \[ em\]
</dt> <dd>

A coordenada x, em pixels, de um clique do mouse.

</dd> <dt>

*y* \[ em\]
</dt> <dd>

A coordenada y, em pixels, de um clique do mouse.

</dd> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**. O valor padrão é **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta. Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.

 

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseWheel de DISPID \_ .

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

 

 




