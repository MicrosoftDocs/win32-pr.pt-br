---
title: Mensagem de HDM_GETFOCUSEDITEM (commctrl. h)
description: Obtém o item em um controle de cabeçalho que tem o foco. Envie essa mensagem explicitamente ou usando a \_ macro GetFocusedItem do cabeçalho.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- controles de Windows de mensagem de HDM_GETFOCUSEDITEM
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
ms.openlocfilehash: f71b1b374c4d12f6dfb493cb8f8e0ea46d9d48094f0aed3c95a037ab7f3ea4f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006112"
---
# <a name="hdm_getfocuseditem-message"></a>\_Mensagem HDM GETFOCUSEDITEM

Obtém o item em um controle de cabeçalho que tem o foco. Envie essa mensagem explicitamente ou usando a macro [**\_ GetFocusedItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Não usado. Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Não usado. Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do item em foco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre controles de cabeçalho](header-controls.md)
</dt> </dl>

 

 





