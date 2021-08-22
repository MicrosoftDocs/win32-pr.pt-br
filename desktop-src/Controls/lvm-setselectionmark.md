---
title: LVM_SETSELECTIONMARK mensagem (Commctrl.h)
description: Define a marca de seleção em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a macro ListView \_ SetSelectionMark.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c80f1392b5bb8b8ae49eaefb639a60213b5d4a7deaf153b99262bf608a770e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217356"
---
# <a name="lvm_setselectionmark-message"></a>Mensagem LVM \_ SETSELECTIONMARK

Define a marca de seleção em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a macro [**ListView \_ SetSelectionMark.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Índice baseado em zero da nova marca de seleção. Se definido como -1, a marca de seleção será removida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a marca de seleção anterior ou -1 se não houver nenhuma marca de seleção anterior.

## <a name="remarks"></a>Comentários

A *marca de seleção* é o índice de item do qual uma seleção múltipla é iniciada. Essa mensagem não afeta o estado de seleção do item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVM \_ GETSELECTIONMARK**](lvm-getselectionmark.md)
</dt> </dl>

 

 





