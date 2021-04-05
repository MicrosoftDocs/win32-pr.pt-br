---
title: Mensagem de LVM_SETITEMPOSITION32 (commctrl. h)
description: Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- Controles de LVM_SETITEMPOSITION32 de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009426"
---
# <a name="lvm_setitemposition32-message"></a>\_Mensagem SETITEMPOSITION32 LVM

Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno). Essa mensagem difere da mensagem [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) , pois usa coordenadas de 32 bits. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItemPosition32 do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item de exibição de lista para o qual definir a posição.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que contém a nova posição do item, em coordenadas de exibição de lista.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

