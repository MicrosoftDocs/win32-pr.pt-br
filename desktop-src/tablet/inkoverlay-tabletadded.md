---
description: Ocorre quando um IInkTablet é adicionado ao sistema.
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: Evento InkOverlay. TabletAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c2faadcbf87e0772afb8f417c97a4be546e08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748481"
---
# <a name="inkoverlaytabletadded-event"></a>Evento InkOverlay. TabletAdded

Ocorre quando um [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é adicionado ao sistema.

## <a name="syntax"></a>Sintaxe


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tablet* \[ no\]
</dt> <dd>

O objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que foi adicionado ao sistema.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICETabletAdded de DISPID \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Interface IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




