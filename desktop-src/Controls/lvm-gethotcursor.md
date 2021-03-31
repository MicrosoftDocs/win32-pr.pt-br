---
title: Mensagem de LVM_GETHOTCURSOR (commctrl. h)
description: Recupera o valor HCURSOR usado quando o ponteiro está sobre um item enquanto o controle ativo está habilitado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetHotCursor do ListView.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- Controles de LVM_GETHOTCURSOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645026"
---
# <a name="lvm_gethotcursor-message"></a>\_Mensagem GETHOTCURSOR LVM

Recupera o valor HCURSOR usado quando o ponteiro está sobre um item enquanto o controle ativo está habilitado. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetHotCursor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor HCURSOR que é o identificador para o cursor que o controle List-View usa quando o controle de acesso está habilitado.

## <a name="remarks"></a>Comentários

Um controle de exibição de lista usa rastreamento dinâmico e seleção de foco quando o estilo [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) é definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





