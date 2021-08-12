---
title: LVM_GETSELECTIONMARK mensagem (Commctrl.h)
description: Recupera a marca de seleção de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView GetSelectionMark.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK controles Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2675550ebc4cf456b439a2e5869068e983f46c82bf6fdde99d8b92806e6cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670974"
---
# <a name="lvm_getselectionmark-message"></a>Mensagem LVM \_ GETSELECTIONMARK

Recupera a marca de seleção de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ListView GetSelectionMark.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a marca de seleção baseada em zero ou -1 se não houver nenhuma marca de seleção.

## <a name="remarks"></a>Comentários

A *marca de seleção* é o índice de item do qual uma seleção múltipla é iniciada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVM \_ SETSELECTIONMARK**](lvm-setselectionmark.md)
</dt> </dl>

 

 





