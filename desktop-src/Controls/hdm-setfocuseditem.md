---
title: Mensagem de HDM_SETFOCUSEDITEM (commctrl. h)
description: Define o foco para um item especificado em um controle de cabeçalho. Envie essa mensagem explicitamente ou usando a \_ macro SetFocusedItem do cabeçalho.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- Controles de HDM_SETFOCUSEDITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086093"
---
# <a name="hdm_setfocuseditem-message"></a>\_Mensagem HDM SETFOCUSEDITEM

Define o foco para um item especificado em um controle de cabeçalho. Envie essa mensagem explicitamente ou usando a macro [**\_ SetFocusedItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Não usado. Deve ser zero.</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

O índice do item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

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

 

 





