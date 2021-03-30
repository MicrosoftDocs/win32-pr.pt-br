---
title: Mensagem de LVM_SETHOTCURSOR (commctrl. h)
description: Define o valor de HCURSOR que o controle de exibição de lista usa quando o ponteiro está sobre um item enquanto o controle ativo está habilitado.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- Controles de LVM_SETHOTCURSOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644261"
---
# <a name="lvm_sethotcursor-message"></a>\_Mensagem SETHOTCURSOR LVM

Define o valor de HCURSOR que o controle de exibição de lista usa quando o ponteiro está sobre um item enquanto o controle ativo está habilitado. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetHotCursor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) . Para verificar se o rastreamento dinâmico está habilitado, chame [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o cursor a ser definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor HCURSOR que é o cursor quente anterior.

## <a name="remarks"></a>Comentários

Um controle de exibição de lista usa rastreamento dinâmico e seleção de foco quando o estilo [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) é definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

