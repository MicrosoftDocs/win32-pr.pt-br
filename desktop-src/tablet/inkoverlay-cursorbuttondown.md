---
description: Ocorre quando a classe InkCollector detecta um botão de cursor que está inoperante.
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: Evento InkOverlay. CursorButtonDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393949be4d7b0f172805aa0b81ce86eac3cf3b3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747445"
---
# <a name="inkoverlaycursorbuttondown-event"></a>Evento InkOverlay. CursorButtonDown

Ocorre quando a [**classe InkCollector**](inkcollector-class.md) detecta um botão de cursor que está inoperante.

## <a name="syntax"></a>Sintaxe


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ no\]
</dt> <dd>

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**CursorButtonDown**](inkcollector-cursorbuttondown.md) .

</dd> <dt>

*Botão* \[ no\]
</dt> <dd>

O botão que foi pressionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Um botão em uma dica de caneta fica inoperante quando o usuário abaixa a caneta para o digitalizador e começa a rastrear um traço. Um botão em um cilindro fica inativo quando o botão é pressionado.

Quando você pressiona o botão direito do mouse, você realmente recebe dois eventos [**CursorButtonDown**](inkcollector-cursorbuttondown.md) – um para o botão direito pressionado e outro para o botão esquerdo pressionado.

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICECursorButtonDown de DISPID \_ .

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

[**Evento CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




