---
description: Evento InkCollector. DoubleClick – ocorre quando o objeto InkCollector ou InkOverlay é clicado duas vezes.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Evento InkCollector. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f0d523ac34f22da1ce37bf106e980343fb12f09cd8fcfe2bb4be454769bf9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718162"
---
# <a name="inkcollectordoubleclick-event"></a>Evento InkCollector. DoubleClick

Ocorre quando o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) é clicado duas vezes.

## <a name="syntax"></a>Sintaxe


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEDblClick de DISPID \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> </dl>

 

 




