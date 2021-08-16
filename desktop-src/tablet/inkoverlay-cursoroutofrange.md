---
description: Evento InkOverlay.CursorOutOfRange – ocorre quando o cursor sai do intervalo de detecção física (proximidade) do contexto do tablet.
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: Evento InkOverlay.CursorOutOfRange (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5774b7f81b1a914dc14ca557db077a0dcf802b02333d8038d0a9194dfa100992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219597"
---
# <a name="inkoverlaycursoroutofrange-event"></a>Evento InkOverlay.CursorOutOfRange

Ocorre quando o cursor sai do intervalo de detecção física (proximidade) do contexto do tablet.

## <a name="syntax"></a>Sintaxe


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**CursorOutOfRange.**](inkcollector-cursoroutofrange.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents \_ e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ ICECursorOutOfRange.

O [**evento CursorOutOfRange**](inkcollector-cursoroutofrange.md) é acionado mesmo quando está no modo de seleção ou apagamento, não apenas quando está no modo de tinta. Isso exige que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento. A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior reconhecimento de eventos da plataforma.

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

[**Evento CursorInRange**](inkcollector-cursorinrange.md)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




