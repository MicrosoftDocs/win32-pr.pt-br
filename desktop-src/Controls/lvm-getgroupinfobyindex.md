---
title: Mensagem de LVM_GETGROUPINFOBYINDEX (commctrl. h)
description: Obtém informações sobre um grupo especificado. Envie essa mensagem explicitamente ou usando a \_ macro GetGroupInfoByIndex do ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- controles de Windows de mensagem de LVM_GETGROUPINFOBYINDEX
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482683e9d1026c1deed17bf1f05310d63ac2127a6a2a6f32b5b5d95a0fbbea3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877396"
---
# <a name="lvm_getgroupinfobyindex-message"></a>\_Mensagem GETGROUPINFOBYINDEX LVM

Obtém informações sobre um grupo especificado. Envie essa mensagem explicitamente ou usando a macro [**\_ GetGroupInfoByIndex do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O índice do grupo.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) para receber informações sobre o grupo especificado por *wParam*. O processo de chamada é responsável por alocar memória para a estrutura e quaisquer buffers na estrutura, como aquele apontado pelo membro **pszHeader** . Defina quaisquer membros contingentes da estrutura, como **cchHeader** o tamanho do buffer apontado por **pszHeader** em **WCHAR** , incluindo o **nulo** de terminação. Defina **cbSize** como sizeof (LVGROUP).

O receptor da mensagem é responsável por definir os membros da estrutura com informações para o grupo especificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





