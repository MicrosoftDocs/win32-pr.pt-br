---
description: Evento InkPicture.SelectionResized – ocorre quando o tamanho da seleção atual foi alterado, por exemplo, por meio de alterações na interface do usuário, procedimentos de recortar e colar ou na propriedade Seleção.
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: Evento InkPicture.SelectionResized (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e67bc19d4d35c356e0774f0843ba62432606c1ee4f1f84095e64c4808d09bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451045"
---
# <a name="inkpictureselectionresized-event"></a>Evento InkPicture.SelectionResized

Ocorre quando o tamanho da seleção atual foi alterado, por exemplo, por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a [**propriedade Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintaxe


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OldSelectionRect* \[ Em\]
</dt> <dd>

O retângulo delimitar da coleção [InkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada como ela existia antes do **evento SelectionResized** ser disparado.

> [!Note]  
> Esse retângulo é especificado em coordenadas de espaço de tinta, o que permite desfazer cenários.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de \_ DISPID IOESelectionResized.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Controle \[ InkPicture da propriedade Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**Classe InkRectangle**](inkrectangle-class.md)
</dt> </dl>

 

