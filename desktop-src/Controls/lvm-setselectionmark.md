---
title: Mensagem de LVM_SETSELECTIONMARK (commctrl. h)
description: Define a marca de seleção em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetSelectionMark do ListView.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- Controles de LVM_SETSELECTIONMARK de mensagens do Windows
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
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644258"
---
# <a name="lvm_setselectionmark-message"></a>\_Mensagem SETSELECTIONMARK LVM

Define a marca de seleção em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetSelectionMark do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base zero da nova marca de seleção. Se definido como-1, a marca de seleção será removida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a marca de seleção anterior ou-1 se não houver marca de seleção anterior.

## <a name="remarks"></a>Comentários

A *marca de seleção* é o índice de item do qual uma seleção múltipla é iniciada. Esta mensagem não afeta o estado de seleção do item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_GETSELECTIONMARK LVM**](lvm-getselectionmark.md)
</dt> </dl>

 

 





