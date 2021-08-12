---
description: Evento InkPicture.CursorButtonUp – ocorre quando o InkCollector detecta um botão de cursor que está em atividade.
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: Evento InkPicture.CursorButtonUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a84a5d8529ecf6387d3832608ae3821be9d317fef46211a6824bddc2ee9574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451075"
---
# <a name="inkpicturecursorbuttonup-event"></a>Evento InkPicture.CursorButtonUp

Ocorre quando o [**InkCollector**](inkcollector-class.md) detecta um botão de cursor que está para cima.

## <a name="syntax"></a>Sintaxe


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorButtonUp.**

</dd> <dt>

*Botão* \[ Em\]
</dt> <dd>

O botão que foi liberado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Um botão em uma dica de caneta é up quando o usuário conclui um traço e eleva a caneta do digitalizador. Um botão em um cilindro fica em cima quando o botão não é pressionado.

Quando você libera o botão direito do mouse, na verdade, recebe dois eventos **CursorButtonUp:** um para o botão direito para cima e outro para o botão esquerdo para cima.

Esse método de evento é definido nas dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** com uma ID de DISPID \_ ICECursorButtonUp.

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

[**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorDown**](inkpicture-cursordown.md)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




