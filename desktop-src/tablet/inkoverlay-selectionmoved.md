---
description: Evento InkOverlay.SelectionMoved – ocorre quando a posição da seleção atual foi alterada, como por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a propriedade Selection.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Evento InkOverlay.SelectionMoved (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e1c9501a9670ebfa89cdcf30fac7a1044450cef932e7c7abb522a5199fd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032064"
---
# <a name="inkoverlayselectionmoved-event"></a>Evento InkOverlay.SelectionMoved

Ocorre quando a posição da seleção atual foi alterada, como por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a [**propriedade Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Sintaxe


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OldSelectionRect* \[ Em\]
</dt> <dd>

O retângulo delimitar da coleção [InkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada como ela existia antes do **evento SelectionMoved** ser disparado.

> [!Note]  
> Esse retângulo é especificado em coordenadas de espaço de tinta, o que permite desfazer cenários.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição \_ IInkOverlayEvents \_ e IInkPictureEvents (dispinterfaces) com uma ID de \_ DISPID IOESelectionMoved.

Para obter o novo retângulo delimitar da coleção de traços que foram movidos, chame o [**método Selection.GetBoundingBox.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)

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

 

