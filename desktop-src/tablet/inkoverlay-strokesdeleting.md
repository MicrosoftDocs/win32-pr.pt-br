---
description: Ocorre antes de os traços serem excluídos da Propriedade Ink.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922482"
---
# <a name="inkoverlaystrokesdeleting-event"></a>Evento InkOverlay. StrokesDeleting

Ocorre antes de os traços serem excluídos da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .

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

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOEStrokesDeleting.

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

[**Classe de propriedade de tinta \[ InkCollector/InkOverLay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 

