---
title: HDM_SETFOCUSEDITEM mensagem (Commctrl.h)
description: Define o foco como um item especificado em um controle de header. Envie essa mensagem explicitamente ou usando a \_ macro Header SetFocusedItem.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- HDM_SETFOCUSEDITEM controles de Windows mensagem
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
ms.openlocfilehash: 9ea853cf625473bee608111eddf877eb09457ee5c2ac6089542b5add0a212195
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171071"
---
# <a name="hdm_setfocuseditem-message"></a>Mensagem HDM \_ SETFOCUSEDITEM

Define o foco como um item especificado em um controle de header. Envie essa mensagem explicitamente ou usando a [**macro \_ Header SetFocusedItem.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Não usado. Deve ser zero.</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

O índice do item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre controles de header](header-controls.md)
</dt> </dl>

 

 





