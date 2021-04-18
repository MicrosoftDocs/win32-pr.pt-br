---
description: Ocorre quando o usuário desenha um novo traço em qualquer mesa digitalizadora.
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: Evento InkPicture. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b85d2410141c2d6d5f7ae92408b7d6da49a447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798219"
---
# <a name="inkpicturestroke-event"></a>Evento InkPicture. Stroke

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

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **Stroke** .

</dd> <dt>

*Traço* \[ no\]
</dt> <dd>

O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado.

</dd> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

**Variante \_ TRUE** para cancelar a coleção do traço; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICEStroke de DISPID \_ .

O evento **Stroke** ocorre no modo de seleção ou apagamento, não apenas ao inserir tinta. Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento. A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.

> [!Note]  
> O evento **Stroke** ocorre quando o usuário termina de desenhar um traço, não quando um traço é adicionado à coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . Quando o usuário começa a desenhar um traço pela primeira vez, ele é adicionado imediatamente à coleção InkStrokes; no entanto, o evento **Stroke** não ocorre até que o traço seja concluído. Portanto, os traços podem existir na coleção InkStrokes que o manipulador de eventos **Stroke** não viu.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Controle InkPicture de evento StrokesAdded \[\]**](inkpicture-strokesadded.md)
</dt> <dt>

[**Controle InkPicture de evento StrokesDeleted \[\]**](inkpicture-strokesdeleted.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

