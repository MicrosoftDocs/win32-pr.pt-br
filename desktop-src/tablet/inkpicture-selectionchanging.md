---
description: Ocorre quando a seleção de tinta no controle InkPicture está prestes a ser modificada, como por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a propriedade Selection.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Evento InkPicture.SelectionChanging (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5960fd212b4362f697c1c83b1bc03729cb9d619081ee6c4895a01a7d7124dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042058"
---
# <a name="inkpictureselectionchanging-event"></a>Evento InkPicture.SelectionChanging

Ocorre quando a seleção de tinta no controle [InkPicture](inkpicture-control-reference.md) está prestes a ser modificada, como por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a [**propriedade Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintaxe


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nova Seleção* \[ Em\]
</dt> <dd>

A nova coleção de [InkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está sendo selecionada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de \_ DISPID IOESelectionChanging.

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
</dt> <dt>

[**Controle \[ InkPicture da propriedade Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

