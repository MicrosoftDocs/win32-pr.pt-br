---
description: Preterido. O PenInputPanel foi substituído pelo painel de entrada de texto (TIP). Ocorre quando o objeto PenInputPanel é alterado entre layouts.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel. Panelchanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f722609ae71761a2a2a05c743aba7bfd83b7d4ff8689333bf2093d4dc21345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856515"
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

## <a name="return-value"></a>Valor retornado

Se esse evento for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Ao criar um objeto [**PenInputPanel**](peninputpanel-class.md) , o [**manuscrito**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) é o **PanelType** padrão. Se você alterar o painel definindo a propriedade [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) antes que o painel de entrada da caneta se torne ativo pela primeira vez, ocorrerá um evento **panelchanged** .

O evento **panelchanged** não é gerado quando o usuário muda entre os pads de escrita alinhado e na caixa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 
