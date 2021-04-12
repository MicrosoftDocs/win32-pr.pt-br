---
description: Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: Evento InkPicture. SelectionMoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25810b87d5a0a3554c46b1a3869bb9b6c88d2fb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297024"
---
# <a name="inkpictureselectionmoved-event"></a>Evento InkPicture. SelectionMoved

Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Sintaxe


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OldSelectionRect* \[ no\]
</dt> <dd>

O retângulo delimitador da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada como existia antes de o evento **SelectionMoved** ser acionado.

> [!Note]  
> Esse retângulo é especificado em coordenadas de espaço de tinta, o que permite cenários de desfazer.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOESelectionMoved.

Para obter o novo retângulo delimitador da coleção de traços que foram movidos, chame o método [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .

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
</dt> <dt>

[**Controle de propriedade de seleção \[ InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**Classe InkRectangle**](inkrectangle-class.md)
</dt> </dl>

 

