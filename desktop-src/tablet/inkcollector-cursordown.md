---
description: Evento InkCollector.CursorDown – ocorre quando a dica de cursor contata a superfície de tablet de digitalização.
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: Evento InkCollector.CursorDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a98a58ce3c6576b45b4c60d47781f8de6ae9f8d5ab0cfea3222ef36890290f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032114"
---
# <a name="inkcollectorcursordown-event"></a>Evento InkCollector.CursorDown

Ocorre quando a dica de cursor contata a superfície de tablet de digitalização.

## <a name="syntax"></a>Sintaxe


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o **evento CursorDown.**

</dd> <dt>

*Traço* \[ Em\]
</dt> <dd>

O [**objeto IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que foi iniciado quando o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) causou o disparo do evento **CursorDown.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido em \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents. As \_ interfaces IInkCollectorEvents, \_ IInkOverlayEvents \_ e IInkPictureEvents implementam a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de DISPID \_ ICECursorDown.

Use esse evento com cuidado porque ele poderá ter um efeito adverso no desempenho da tinta se muito código for executado nos manipuladores de eventos. Para melhorar o desempenho de tinta em tempo real, o oculta ou mostra o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Evento CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkRogkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

