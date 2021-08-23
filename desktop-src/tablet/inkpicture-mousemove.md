---
description: Ocorre quando o ponteiro do mouse é movido sobre o controle InkPicture.
ms.assetid: b4c703da-0e4a-4d4c-9a6c-0e002344fb2f
title: Evento InkPicture. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd7a45d8c2829dd9721eebed918b54a9ad7fbb505988bc538563fefc46e33da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032044"
---
# <a name="inkpicturemousemove-event"></a>Evento InkPicture. MouseMove

Ocorre quando o ponteiro do mouse é movido sobre o controle [InkPicture](inkpicture-control-reference.md) .

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

O botão que foi pressionado.

</dd> <dt>

*Shift* \[ no\]
</dt> <dd>

O estado da tecla SHIFT.

</dd> <dt>

*PX* \[ no\]
</dt> <dd>

A coordenada x, em pixels, do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*pY* \[ no\]
</dt> <dd>

A coordenada y, em pixels, do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

**Variante \_ TRUE** para cancelar este evento para o controle pai; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Os parâmetros *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao sistema de coordenadas do espaço de tinta. Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo que não reconhece a caneta e esse tipo de aplicativo refere-se apenas a pixels.

 

> [!Caution]  
> Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkpicture-mousedown.md), **MouseMove** e [**MouseUp**](inkpicture-mouseup.md) . Cancelar alguns desses eventos pode ter resultados imprevistos.

 

Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEMouseDown DISPID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

