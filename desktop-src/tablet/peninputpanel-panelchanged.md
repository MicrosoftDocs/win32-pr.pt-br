---
description: Preterido. O PenInputPanel foi substituído pelo painel de entrada de texto (TIP). Ocorre quando o objeto PenInputPanel é alterado entre layouts.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel. Panelchanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297223"
---
# <a name="peninputpanelpanelchanged-event"></a>Evento PenInputPanel. Panelchanged

Preterido. O [**PenInputPanel**](peninputpanel-class.md) foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).

Ocorre quando o objeto [**PenInputPanel**](peninputpanel-class.md) é alterado entre layouts.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewPanelType* \[ no\]
</dt> <dd>

O novo tipo de painel usado para entrada dentro do objeto [**PenInputPanel**](peninputpanel-class.md) , após o evento **panelchanged** ser acionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse evento for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Ao criar um objeto [**PenInputPanel**](peninputpanel-class.md) , o [**manuscrito**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) é o **PanelType** padrão. Se você alterar o painel definindo a propriedade [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) antes que o painel de entrada da caneta se torne ativo pela primeira vez, ocorrerá um evento **panelchanged** .

O evento **panelchanged** não é gerado quando o usuário muda entre os pads de escrita alinhado e na caixa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 
