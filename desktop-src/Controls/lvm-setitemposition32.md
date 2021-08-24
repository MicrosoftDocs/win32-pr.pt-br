---
title: Mensagem de LVM_SETITEMPOSITION32 (commctrl. h)
description: Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- controles de Windows de mensagem de LVM_SETITEMPOSITION32
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
ms.openlocfilehash: 737b9aa78067bd4851c907da4ac51bd2645a833d8f3335c90a6e81a902d3a30a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656246"
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

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

