---
description: Ocorre quando um usuário clica no controle InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Evento InkPicture.Click (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ebde47609a36a92eca211f597345a9784fca03f66076ebb4db6f04ee6f5936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218535"
---
# <a name="inkpictureclick-event"></a>Evento InkPicture.Click

Ocorre quando um usuário clica no [controle InkPicture.](inkpicture-control-reference.md)

## <a name="syntax"></a>Sintaxe


```C++
void Click();
```



## <a name="parameters"></a>Parâmetros

Esse evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Clicar em um controle gera eventos [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp,**](inkpicture-mouseup.md) além do evento Click.

> [!Note]  
> Para distinguir entre os botões esquerdo, direito e meio do mouse, use os [**eventos MouseDown**](inkpicture-mousedown.md) e [**MouseUp.**](inkpicture-mouseup.md)

 

Se houver código no evento **Click,** o evento [**DblClick**](inkpicture-dblclick.md) nunca será disparado, pois o evento **Click** é o primeiro evento a ser disparado entre os dois. Como resultado, o clique do mouse é interceptado pelo evento **Click,** para que o **evento DblClick** não ocorra.

Esse método de evento é definido na interface **\_ IInkPictureEvents.** A interface **\_ IInkPictureEvents** implementa a interface IDispatch com um identificador **dispID \_ IPEClick.**

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

 

 




