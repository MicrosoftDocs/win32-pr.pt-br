---
description: Evento InkOverlay. Stroke – ocorre quando o usuário desenha um novo traço em qualquer Tablet.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Evento InkOverlay. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2836699591b4f1a87ce3d206a795eb13be188def28ea3eadef687a1d96024ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712626"
---
# <a name="inkoverlaystroke-event"></a>Evento InkOverlay. Stroke

Ocorre quando o usuário desenha um novo traço em qualquer mesa digitalizadora.

## <a name="syntax"></a>Sintaxe


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ no\]
</dt> <dd>

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**Stroke**](inkcollector-stroke.md) .

</dd> <dt>

*Traço* \[ no\]
</dt> <dd>

O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado.

</dd> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

Especifica se o evento deve ser cancelado. Se **for true**, a coleção do traço será cancelada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICEStroke de DISPID \_ .

O evento [**Stroke**](inkcollector-stroke.md) é acionado no modo de seleção ou apagamento, não apenas ao inserir tinta. Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento. A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.

> [!Note]  
> O evento [**Stroke**](inkcollector-stroke.md) é acionado quando o usuário termina de desenhar um traço, não quando um traço é adicionado à coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . Quando o usuário começa a desenhar um traço pela primeira vez, ele é adicionado imediatamente à coleção InkStrokes; no entanto, o evento **Stroke** não é acionado até que o traço seja concluído. Portanto, os traços podem existir na coleção InkStrokes que o manipulador de eventos **Stroke** não viu.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Coleção de InkStrokes de eventos StrokesAdded \[\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**Classe InkOverlay do evento StrokesDeleted \[\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

