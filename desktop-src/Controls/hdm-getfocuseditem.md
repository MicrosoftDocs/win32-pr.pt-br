---
title: Mensagem de HDM_GETFOCUSEDITEM (commctrl. h)
description: Obtém o item em um controle de cabeçalho que tem o foco. Envie essa mensagem explicitamente ou usando a \_ macro GetFocusedItem do cabeçalho.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- Controles de HDM_GETFOCUSEDITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455436"
---
# <a name="hdm_getfocuseditem-message"></a>\_Mensagem HDM GETFOCUSEDITEM

Obtém o item em um controle de cabeçalho que tem o foco. Envie essa mensagem explicitamente ou usando a macro [**\_ GetFocusedItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Não usado. Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Não usado. Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item em foco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre controles de cabeçalho](header-controls.md)
</dt> </dl>

 

 





