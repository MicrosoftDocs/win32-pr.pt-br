---
title: Mensagem de TCM_SETTOOLTIPS (commctrl. h)
description: Atribui um controle ToolTip a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetToolTips do TabCtrl.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- Controles de TCM_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644242"
---
# <a name="tcm_settooltips-message"></a>Mensagem do TCM \_ SETtooltips

Atribui um controle ToolTip a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetToolTips do TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para o controle ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Você pode recuperar o controle de dica de ferramenta associado a um controle guia usando a mensagem [**TCM \_ GetToolTips**](tcm-gettooltips.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





