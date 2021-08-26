---
description: Ocorre quando a seleção de tinta no controle InkPicture foi alterada, como por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a propriedade Selection.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: Evento InkPicture.SelectionChanged (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1fce27d9aa0dd043c5e474d790c1bd9737a9c10bffbed3eff6a287be67030f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938996"
---
# <a name="inkpictureselectionchanged-event"></a>Evento InkPicture.SelectionChanged

Ocorre quando a seleção de tinta no controle [InkPicture](inkpicture-control-reference.md) foi alterada, como por meio de alterações na interface do usuário, procedimentos de recortar e colar ou a [**propriedade Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintaxe


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Parâmetros

Esse evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para obter mais detalhes sobre esse evento, consulte o evento [**SelectionChanged**](inkoverlay-selectionchanged.md) do objeto [**InkOverlay,**](inkoverlay-class.md) que tem a mesma funcionalidade.

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

 

 




