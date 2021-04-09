---
description: Ocorre quando um traço é adicionado ao objeto InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Evento InkDisp. InkAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010463"
---
# <a name="inkdispinkadded-event"></a>Evento InkDisp. InkAdded

Ocorre quando um traço é adicionado ao objeto [**InkDisp**](inkdisp-class.md) .

## <a name="syntax"></a>Sintaxe


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StrokeIds* \[ no\]
</dt> <dd>

A matriz de inteiros de informações de ID de traço para todos os traços que foram adicionados quando esse evento ocorre.

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Se você usar o objeto [**InkOverlay**](inkoverlay-class.md) ou o [controle InkPicture](inkpicture-control-reference.md) (em que [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) é igual a [**delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) e [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) é igual a [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) e passar a borracha sobre um traço, você obterá a seguinte sequência de eventos:

-   [**InkDeleted**](inkdisp-inkdeleted.md)
-   **InkAdded**
-   [**InkDeleted**](inkdisp-inkdeleted.md)

Os eventos **InkAdded** e [**InkDeleted**](inkdisp-inkdeleted.md) adicionais ocorrem porque o código subjacente adiciona um traço interno e invisível para rastrear a borracha.

Esse método de evento é definido na \_ interface IInkEvents. A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IEInkAdded DISPID.

O evento **InkAdded** é acionado mesmo quando no modo de seleção ou apagamento, não apenas ao inserir tinta. Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento. A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Classe InkOverlay da propriedade EditingMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**Classe InkOverlay da Propriedade EraserMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**Evento InkDeleted**](inkdisp-inkdeleted.md)
</dt> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[Referência de controle InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

