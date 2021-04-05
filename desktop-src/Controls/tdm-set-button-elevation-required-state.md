---
title: Mensagem de TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (commctrl. h)
description: Especifica se um determinado botão de diálogo de tarefa ou link de comando deve ter um ícone de escudo de UAC (controle de conta de usuário); ou seja, se a ação invocada pelo botão requer elevação.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- Controles de TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086320"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>\_Mensagem de \_ \_ \_ estado necessário de elevação do botão \_ de TDM Set

Especifica se um determinado botão de diálogo de tarefa ou link de comando deve ter um ícone de escudo de UAC (controle de conta de usuário); ou seja, se a ação invocada pelo botão requer elevação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

A ID do botão de ação ou link de comando a ser atualizado.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Defina como 0 para designar que a ação invocada pelo botão não requer elevação. Defina como diferente de zero para designar que a ação requer elevação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





