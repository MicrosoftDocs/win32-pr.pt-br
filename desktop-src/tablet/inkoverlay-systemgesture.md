---
description: InkOverlay.Sysevento temGesture – ocorre quando um gesto do sistema é reconhecido.
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay.Sysevento temGesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e1e55048a60edef4344ec3b566b08de29d9f3d0a16ccccc1f3094949c2aec86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218759"
---
# <a name="inkoverlaysystemgesture-event"></a>InkOverlay.Sysevento temGesture

Ocorre quando um gesto do sistema é reconhecido.

## <a name="syntax"></a>Sintaxe


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o [**evento SystemGesture.**](inkcollector-systemgesture.md)

</dd> <dt>

*ID* \[ em\]
</dt> <dd>

O valor do gesto do sistema.

</dd> <dt>

*X* \[ em\]
</dt> <dd>

A coordenada X do local do gesto.

</dd> <dt>

*Y* \[ em\]
</dt> <dd>

A coordenada Y do local do gesto.

</dd> <dt>

*Modificador* \[ Em\]
</dt> <dd>

Reservado.

</dd> <dt>

*Caractere* \[ Em\]
</dt> <dd>

Reservado.

</dd> <dt>

*CursorMode* \[ Em\]
</dt> <dd>

Um valor que indica se o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está no modo normal ou no modo de borracha. 1 é para o modo normal e 2 são para o modo de borracha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Os gestos do sistema são úteis porque eles dão informações sobre o [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que está sendo usado para criar o gesto. Eles também fornecem atalhos para combinações de eventos do mouse e são maneiras "mais baratas" de detectar eventos do mouse.

Por exemplo, em vez de procurar um par de eventos mousedown do evento [**MouseUp**](inkcollector-mouseup.md)sem outros eventos do mouse que ocorrem entre eles, você pode procurar os gestos do sistema Toque ou  /  [](inkcollector-mousedown.md) **RightTap.** [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

Como outro exemplo, em vez de escutar eventos de evento [**MouseMove**](inkcollector-mousedown.md)mouseDown e obter várias mensagens de Evento  /  [](inkcollector-mousemove.md) **MouseMove,** você pode observar os gestos do sistema [**Arrastar**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightDrag,** desde que não esteja interessado nas coordenadas (x, y) de cada posição do mouse. Isso permite que você receba apenas uma mensagem em vez de várias mensagens de Evento **MouseMove.**

Para ver uma lista de gestos específicos do sistema, consulte o tipo de enumeração [**InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Para obter mais informações sobre gestos do sistema, [consulte Usando gestos](using-gestures.md) e [entrada de comando no tablet pc](/previous-versions//dd314533(v=vs.85)).

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ ICESystemGesture.

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

[**Enumeração InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Usando gestos](using-gestures.md)
</dt> <dt>

[Entrada de caneta, tinta e reconhecimento](pen-input--ink--and-recognition.md)
</dt> <dt>

[Entrada de comando no tablet](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

