---
title: Mensagem de TCM_GETTOOLTIPS (commctrl. h)
description: Recupera o identificador para o controle de dica de ferramenta associado a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetToolTips TabCtrl.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- Controles de TCM_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086241"
---
# <a name="tcm_gettooltips-message"></a>Mensagem do TCM \_ GETtooltips

Recupera o identificador para o controle de dica de ferramenta associado a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetToolTips TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de dica de ferramenta se for bem-sucedido ou **NULL** de outra forma.

## <a name="remarks"></a>Comentários

Um controle guia cria um controle ToolTip se ele tiver o estilo de [**\_ Tooltips de TCS**](tab-control-styles.md) . Você também pode atribuir um controle de dica de ferramenta a um controle guia usando a mensagem [**TCM \_ SetToolTips**](tcm-settooltips.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





