---
title: Mensagem de LVM_GETGROUPINFOBYINDEX (commctrl. h)
description: Obtém informações sobre um grupo especificado. Envie essa mensagem explicitamente ou usando a \_ macro GetGroupInfoByIndex do ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- Controles de LVM_GETGROUPINFOBYINDEX de mensagens do Windows
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
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085815"
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

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





