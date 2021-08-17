---
title: LVM_SETTEXTCOLOR mensagem (Commctrl.h)
description: Define a cor do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro ListView \_ SetTextColor.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- LVM_SETTEXTCOLOR controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70cb9de975440a4093ef8c88992305d294cc04f362c8e9ccb3434937b78f007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217366"
---
# <a name="lvm_settextcolor-message"></a>Mensagem LVM \_ SETTEXTCOLOR

Define a cor do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a [**macro ListView \_ SetTextColor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um [**COLORREF**](/windows/desktop/gdi/colorref) que especifica a nova cor do texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

