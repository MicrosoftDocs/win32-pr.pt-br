---
description: Evento InkOverlay.SelectionResizing – ocorre quando o tamanho da seleção atual está prestes a mudar, como por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a propriedade Seleção.
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: Evento InkOverlay.SelectionResizing (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260ac01f303b7f6ced5f38c77bc2d490d1e99aa53382ebe7d2daf52f986ccf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712676"
---
# <a name="inkoverlayselectionresizing-event"></a>Evento InkOverlay.SelectionResizing

Ocorre quando o tamanho da seleção atual está prestes a mudar, como por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a [**propriedade Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Sintaxe


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CurSelectionRect* \[ Em\]
</dt> <dd>

O retângulo delimitar da seleção após o **evento SelectionResizing.**

> [!Note]  
> Esse retângulo é especificado nas coordenadas da janela do cliente, o que permite cenários como manter a taxa de proporção ao reizing.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição \_ IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de \_ DISPID IOESelectionResizing.

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

[**Propriedade Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**Classe InkRectangle**](inkrectangle-class.md)
</dt> </dl>

 

 




