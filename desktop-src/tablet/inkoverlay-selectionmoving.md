---
description: Ocorre quando a posição da seleção atual está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: Evento InkOverlay. SelectionMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afc77198a6a7228e44b3f2bad8015c25a939812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782679"
---
# <a name="inkoverlayselectionmoving-event"></a>Evento InkOverlay. SelectionMoving

Ocorre quando a posição da seleção atual está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .

## <a name="syntax"></a>Sintaxe


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CurSelectionRect* \[ no\]
</dt> <dd>

O retângulo para o qual a seleção é movida após o evento **SelectionMoving** .

> [!Note]  
> Esse retângulo é especificado em coordenadas da janela do cliente, o que permite cenários como manter a taxa de proporção ao redimensionar.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID fora do DISPID \_ IOESelectionMoving.

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

**Classe InkOverlay**
</dt> <dt>

[**Propriedade de seleção**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**Classe InkRectangle**](inkrectangle-class.md)
</dt> </dl>

 

 




