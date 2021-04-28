---
description: InkPicture.Sysevento temGesture – ocorre quando um gesto do sistema é reconhecido.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.Sysevento temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cde11b73b6b0d3861a79538a7f9ee19487b6384
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113684"
---
# <a name="inkpicturesystemgesture-event"></a>InkPicture.Sysevento temGesture

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

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Os gestos do sistema fornecem informações sobre o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que está sendo usado para criar o gesto. Eles também fornecem atalhos para combinações de eventos de mouse e são maneiras de detectar eventos de mouse com menos impacto no desempenho.

Por exemplo, em vez de procurar por um evento [**MouseUp \[ \]**](inkpicture-mouseup.md)controle InkPicture / [**de \[ \] evento**](inkpicture-mousedown.md) de controle de eventos MouseDown com nenhum outro evento de mouse ocorrendo no, você pode procurar os gestos do sistema Tap ou RightTap.

Como outro exemplo, em vez de escutar eventos de controle de InkPicture de [**evento de controle de eventos de \[ \]**](inkpicture-mousedown.md)evento / [**MouseMove \[ \]**](inkpicture-mousemove.md) e obter inúmeras mensagens de **\[ controle \] de InkPicture** de evento MouseMove, você pode observar os gestos do sistema de arrastar ou RightDrag, contanto que não esteja interessado nas coordenadas (x, y) de cada posição do mouse. Isso permite que você receba apenas uma mensagem em vez de várias mensagens de **\[ controle \] de InkPicture de evento MouseMove** .

Para obter uma lista de gestos do sistema específicos, consulte o tipo de enumeração [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Para obter mais informações sobre gestos do sistema, consulte [usando gestos](using-gestures.md) e [entrada de comando no Tablet PC](/previous-versions//dd314533(v=vs.85)).

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICESystemGesture de DISPID \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Enumeração InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[Usando gestos](using-gestures.md)
</dt> </dl>

 

