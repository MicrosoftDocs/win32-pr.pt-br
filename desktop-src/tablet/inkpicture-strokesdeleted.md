---
description: Ocorre depois que os objetos IInkStrkeDisp foram excluídos da propriedade Ink.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: Evento InkPicture.StrokesDeleted (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b2d4f0be69adf6c9c44f3eadec250d8cba3ebb8935bde5c06cd026e478da3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717355"
---
# <a name="inkpicturestrokesdeleted-event"></a>Evento InkPicture.StrokesDeleted

Ocorre depois que [**os objetos IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) foram excluídos da [**propriedade Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)

## <a name="syntax"></a>Sintaxe


```C++
void StrokesDeleted();
```



## <a name="parameters"></a>Parâmetros

Esse evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Não há dados de evento.

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de \_ DISPID IOEOpekesDeleted.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




