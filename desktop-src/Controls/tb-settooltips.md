---
title: Mensagem de TB_SETTOOLTIPS (commctrl. h)
description: Associa um controle ToolTip a uma barra de ferramentas.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- controles de Windows de mensagem de TB_SETTOOLTIPS
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
ms.openlocfilehash: a75827df49eeaf8b6175cd14180ebb26ddbb642588ee77d625c701eee457baaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061226"
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

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Todos os botões adicionados a uma barra de ferramentas antes de enviar a mensagem de **TB \_ SetToolTips** não serão registrados com o controle ToolTip.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





