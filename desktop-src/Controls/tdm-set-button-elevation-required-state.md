---
title: Mensagem de TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (commctrl. h)
description: Especifica se um determinado botão de diálogo de tarefa ou link de comando deve ter um ícone de escudo de UAC (controle de conta de usuário); ou seja, se a ação invocada pelo botão requer elevação.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- controles de Windows de mensagem de TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
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
ms.openlocfilehash: 2c69998da085a74b144179a0a4244c787cd3a871d63eca1e5df9c4e555b1a7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104616"
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

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





