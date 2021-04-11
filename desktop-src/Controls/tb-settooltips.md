---
title: Mensagem de TB_SETTOOLTIPS (commctrl. h)
description: Associa um controle ToolTip a uma barra de ferramentas.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- Controles de TB_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009122"
---
# <a name="tb_settooltips-message"></a>Mensagem de TB \_ SETtooltips

Associa um controle ToolTip a uma barra de ferramentas.

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

Todos os botões adicionados a uma barra de ferramentas antes de enviar a mensagem de **TB \_ SetToolTips** não serão registrados com o controle ToolTip.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





