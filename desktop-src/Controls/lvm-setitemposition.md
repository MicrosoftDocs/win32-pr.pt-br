---
title: Mensagem de LVM_SETITEMPOSITION (commctrl. h)
description: Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno). Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetItemPosition do ListView.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- Controles de LVM_SETITEMPOSITION de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824455"
---
# <a name="lvm_setitemposition-message"></a>\_Mensagem SETITEMPOSITION LVM

Move um item para uma posição especificada em um controle de exibição de lista (deve estar no ícone ou exibição de ícone pequeno). Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItemPosition do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a nova posição x do canto superior esquerdo do item, em coordenadas de exibição. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a nova posição y do canto superior esquerdo do item, em coordenadas de exibição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se o controle de exibição de lista tiver o estilo de [**\_ AutoOrganizar LVS**](list-view-window-styles.md) , os itens no controle de exibição de lista serão organizados depois que a posição do item for definida.

No Windows Vista, o envio dessa mensagem para um controle de exibição de lista com o estilo [**\_ AutoOrganizar LVS**](list-view-window-styles.md) não faz nada e o valor de retorno é **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

