---
title: Mensagem de TBM_SETTIPSIDE (commctrl. h)
description: Posiciona um controle ToolTip usado por um controle TrackBar. Os controles TrackBar que usam o \_ estilo de dicas de ferramenta TBS exibem dicas de ferramenta.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- Controles de TBM_SETTIPSIDE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369418"
---
# <a name="tbm_settipside-message"></a>\_Mensagem tbm SETTIPSIDE

Posiciona um controle ToolTip usado por um controle TrackBar. Os controles TrackBar que usam o estilo de [**\_ dicas de ferramenta TBS**](trackbar-control-styles.md) exibem dicas de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que representa o local no qual exibir o controle ToolTip. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                                   | Significado                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <dt>**TBTS \_ superior**</dt> </dl>          | O controle ToolTip será posicionado acima do TrackBar. Esse sinalizador é para uso com trackbars horizontais.<br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <dt>**TBTS \_ à esquerda**</dt> </dl>       | O controle ToolTip será posicionado à esquerda do TrackBar. Esse sinalizador é para uso com trackbars vertical.<br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <dt>**TBTS \_ inferior**</dt> </dl> | O controle ToolTip será posicionado abaixo do TrackBar. Esse sinalizador é para uso com trackbars horizontais.<br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <dt>**TBTS \_ à direita**</dt> </dl>    | O controle ToolTip será posicionado à direita do TrackBar. Esse sinalizador é para uso com trackbars vertical.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor que representa o local anterior do controle ToolTip. O valor de retorno é igual a um dos valores possíveis para *wParam*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





