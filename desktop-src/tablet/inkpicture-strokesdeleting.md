---
description: Ocorre antes de os objetos IInkStrokeDisp serem excluídos da Propriedade Ink.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: Evento InkPicture. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011478"
---
# <a name="inkpicturestrokesdeleting-event"></a>Evento InkPicture. StrokesDeleting

Ocorre antes de os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) serem excluídos da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .

## <a name="syntax"></a>Sintaxe


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Traços* \[ no\]
</dt> <dd>

A coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) excluída quando o evento **StrokesDeleting** é acionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOEStrokesDeleting.

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

 

