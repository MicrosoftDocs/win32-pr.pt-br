---
title: Mensagem de LVM_GETTOOLTIPS (commctrl. h)
description: Recupera o controle ToolTip que o controle List-View usa para exibir dicas de ferramenta. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetToolTips do ListView.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- Controles de LVM_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455744"
---
# <a name="lvm_gettooltips-message"></a>Mensagem do LVM \_ GETtooltips

Recupera o controle ToolTip que o controle List-View usa para exibir dicas de ferramenta. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetToolTips do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador do controle ToolTip.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**autotooltips do LVM \_**](lvm-settooltips.md)
</dt> </dl>

 

 





