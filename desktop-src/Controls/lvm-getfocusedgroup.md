---
title: LVM_GETFOCUSEDGROUP mensagem (Commctrl.h)
description: Obtém o grupo que tem o foco. Envie essa mensagem explicitamente ou usando a \_ macro ListView GetFocusedGroup.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9b253405683c058518706e92e62f09041ae4db0e4bee426aa653103bda2188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877426"
---
# <a name="lvm_getfocusedgroup-message"></a>Mensagem \_ GETFOCUSEDGROUP LVM

Obtém o grupo que tem o foco. Envie essa mensagem explicitamente ou usando a macro [**\_ ListView GetFocusedGroup.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do grupo com o estado de LVGS FOCUSED ou -1 se não houver nenhum grupo com estado \_ de LVGS \_ FOCUSED.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





