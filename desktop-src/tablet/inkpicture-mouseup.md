---
description: Ocorre quando o ponteiro do mouse é movido sobre o controle InkPicture e um botão do mouse é liberado.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: Evento InkPicture. MouseUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf652e1ad4110afb4819e5326a5a19a894a310a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791584"
---
# <a name="inkpicturemouseup-event"></a>Evento InkPicture. MouseUp

Ocorre quando o ponteiro do mouse é movido sobre o controle [InkPicture](inkpicture-control-reference.md) e um botão do mouse é liberado.

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

**Variante \_ TRUE** para cancelar o evento MouseUp para o controle pai; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Os parâmetros *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao sistema de coordenadas do espaço de tinta. Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo que não reconhece a caneta e esse tipo de aplicativo refere-se apenas a pixels.

 

> [!Caution]  
> Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md)e **MouseUp** . Cancelar alguns desses eventos pode ter resultados imprevistos.

 

Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEMouseDown DISPID.

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

 

