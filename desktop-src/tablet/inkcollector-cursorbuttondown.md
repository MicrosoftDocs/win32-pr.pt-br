---
description: Evento InkCollector. CursorButtonDown – ocorre quando a classe InkCollector detecta um botão de cursor que está inoperante.
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Evento InkCollector. CursorButtonDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c8a2c1a2e832d4fd18c7c84f9905d0aa1694b425f5f5e7ece91e96afc1684f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451289"
---
# <a name="inkcollectorcursorbuttondown-event"></a>Evento InkCollector. CursorButtonDown

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

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorButtonDown** .

</dd> <dt>

*Botão* \[ no\]
</dt> <dd>

O botão que foi pressionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Um botão em uma dica de caneta fica inoperante quando o usuário abaixa a caneta para o digitalizador e começa a rastrear um traço. Um botão em um cilindro fica inativo quando o botão é pressionado.

Quando você pressiona o botão direito do mouse, você realmente recebe dois eventos **CursorButtonDown** – um para o botão direito pressionado e outro para o botão esquerdo pressionado.

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICECursorButtonDown de DISPID \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Evento CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




