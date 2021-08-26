---
title: Mensagem de TCM_SETTOOLTIPS (commctrl. h)
description: Atribui um controle ToolTip a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetToolTips do TabCtrl.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- controles de Windows de mensagem de TCM_SETTOOLTIPS
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
ms.openlocfilehash: c8bfec3b7272ceae3dcbf1781e3bb17a988f2252b3c0a74822677bff6ea39209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104686"
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

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Você pode recuperar o controle de dica de ferramenta associado a um controle guia usando a mensagem [**TCM \_ GetToolTips**](tcm-gettooltips.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





