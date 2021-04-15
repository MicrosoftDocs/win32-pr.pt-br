---
description: Ocorre quando um gesto do sistema é reconhecido.
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.Sysevento temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282f28e5ef1bc3a86f51b6d345be6e00d78c8213
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501620"
---
# <a name="inkcollectorsystemgesture-event"></a>InkCollector.Sysevento temGesture

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

*Cursor* \[ no\]
</dt> <dd>

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **SystemGesture** .

</dd> <dt>

*ID* \[ em\]
</dt> <dd>

O valor do gesto do sistema.

</dd> <dt>

*X* \[ em\]
</dt> <dd>

A coordenada x da localização do gesto.

</dd> <dt>

*Y* \[ em\]
</dt> <dd>

A coordenada y do local do gesto.

</dd> <dt>

*Modificador* \[ no\]
</dt> <dd>

Reservado.

</dd> <dt>

*Caractere* \[ de no\]
</dt> <dd>

Reservado.

</dd> <dt>

*CursorMode* \[ no\]
</dt> <dd>

Um valor que indica se o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está no modo normal ou borracha. 1 é para o modo normal e 2 são para o modo de borracha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Os gestos do sistema são úteis porque fornecem informações sobre o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que está sendo usado para criar o gesto. Eles também fornecem atalhos para combinações de eventos de mouse e são maneiras "mais baratas" de detectar eventos de mouse.

Por exemplo, em vez de procurar por [**um**](inkcollector-mouseup.md)  /  par de eventos [**evento MouseDown**](inkcollector-mousedown.md) evento do MouseUp sem outros eventos de mouse ocorrendo no, você pode procurar os gestos do sistema [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightTap** .

Como outro exemplo, em vez de escutar eventos de evento MouseMove do [**evento MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) e obter inúmeras mensagens de **evento MouseMove** , você pode observar os gestos do sistema de [**arrastar**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightDrag** , contanto que não esteja interessado nas coordenadas (x, y) de cada posição do mouse. Isso permite que você receba apenas uma mensagem em vez de várias mensagens de **evento MouseMove** .

Para obter uma lista de gestos do sistema específicos, consulte o tipo de enumeração [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Para obter mais informações sobre gestos do sistema, consulte [usando gestos](using-gestures.md) e [entrada de comando no Tablet PC](/previous-versions//dd314533(v=vs.85)).

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICESystemGesture de DISPID \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Enumeração InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Usando gestos](using-gestures.md)
</dt> <dt>

[Entrada, tinta e reconhecimento de caneta](pen-input--ink--and-recognition.md)
</dt> <dt>

[Entrada de comando no Tablet PC](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

