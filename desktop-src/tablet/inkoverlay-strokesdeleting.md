---
description: Ocorre antes que os traços sejam excluídos da propriedade Ink.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay.StrokesDeleting (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85e01eabc46e8e9cc4ca844ae8f5efa8b58e83fdee2724792a3856445b7dbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712666"
---
# <a name="inkoverlaystrokesdeleting-event"></a>Evento InkOverlay.StrokesDeleting

Ocorre antes que os traços sejam excluídos da [**propriedade Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)

## <a name="syntax"></a>Sintaxe


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Traços* \[ Em\]
</dt> <dd>

A [coleção InkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) excluída quando o **evento StrokesDeleting** é a incêndio.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição \_ IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de \_ DISPID IOEOpekesDeleting.

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

[**Classe \[ InkCollector/InkOverLay da propriedade Ink\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 

