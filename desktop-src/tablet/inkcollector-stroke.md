---
description: Evento InkCollector.Stroke – ocorre quando o usuário desenha um novo traço em qualquer tablet.
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: Evento InkCollector.Stroke (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3ba434e90d1caca0651429be10a11a27accfff327d22f7aa73dc71b7b145ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220789"
---
# <a name="inkcollectorstroke-event"></a>Evento InkCollector.Stroke

Ocorre quando o usuário desenha um novo traço em qualquer tablet.

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

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o **evento Stroke.**

</dd> <dt>

*Traço* \[ Em\]
</dt> <dd>

O objeto [**IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar o evento; caso contrário, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ ICEOpeke.

O **evento Stroke** é acionado quando está no modo de seleção ou apagamento, não apenas ao inserir tinta. Isso exige que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento. A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior reconhecimento de eventos da plataforma.

> [!Note]  
> O **evento Stroke** é a disparo quando o usuário termina de desenhar um traço, não quando um traço é adicionado à coleção [InkStrkes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Quando o usuário começa a desenhar um traço pela primeira vez, ele é adicionado imediatamente à coleção InkStrkes; no entanto, **o evento Stroke** não é a incêndio até que o traço seja concluído. Portanto, os traços podem existir na coleção InkStrkes que o manipulador de eventos **Stroke** não viu.

 

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

[**Coleção StrokesAdded Event \[ InkStrkes\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**Classe StrokesDeleted Event \[ InkOverlay\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkRogkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

