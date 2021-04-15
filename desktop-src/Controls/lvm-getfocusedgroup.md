---
title: Mensagem de LVM_GETFOCUSEDGROUP (commctrl. h)
description: Obtém o grupo que tem o foco. Envie essa mensagem explicitamente ou usando a macro do ListView \_ Getconcentrour.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- Controles de LVM_GETFOCUSEDGROUP de mensagens do Windows
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
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454629"
---
# <a name="lvm_getfocusedgroup-message"></a>Mensagem do LVM \_ GETfocaling

Obtém o grupo que tem o foco. Envie essa mensagem explicitamente ou usando a macro do [**ListView \_ getconcentrour**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do grupo com o estado de LVGS \_ focalizado ou-1 se não houver nenhum grupo com o estado de LVGS \_ focalizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





