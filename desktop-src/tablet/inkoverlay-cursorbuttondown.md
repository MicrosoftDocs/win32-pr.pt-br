---
description: Evento InkOverlay.CursorButtonDown – ocorre quando a Classe InkCollector detecta um botão de cursor que está inocesto.
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: Evento InkOverlay.CursorButtonDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e73edfd6c8d9901a1eab0adf13c3c5439ef5716d1489ddb30e008079304d44b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967095"
---
# <a name="inkoverlaycursorbuttondown-event"></a>Evento InkOverlay.CursorButtonDown

Ocorre quando a [**Classe InkCollector**](inkcollector-class.md) detecta um botão de cursor que está para baixo.

## <a name="syntax"></a>Sintaxe


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o [**evento CursorButtonDown.**](inkcollector-cursorbuttondown.md)

</dd> <dt>

*Botão* \[ Em\]
</dt> <dd>

O botão que foi pressionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Um botão em uma dica de caneta é pressionado quando o usuário baixa a caneta para o digitalizador e começa a rastrear um traço. Um botão em um cilindro fica ino mouse quando o botão é pressionado.

Quando você pressiona o botão direito do mouse, na verdade, recebe dois eventos [**CursorButtonDown:**](inkcollector-cursorbuttondown.md) um para o botão direito pressionado e outro para o botão esquerdo pressionado.

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents \_ e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ ICECursorButtonDown.

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

[**Evento CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




