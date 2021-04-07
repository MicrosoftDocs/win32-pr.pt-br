---
title: Mensagem de LVM_GETTEXTBKCOLOR (commctrl. h)
description: Recupera a cor da tela de fundo do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTextBkColor do ListView.
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- Controles de LVM_GETTEXTBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bf5b6700904c5af47ef47e749dfa753c5ff8cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918966"
---
# <a name="lvm_gettextbkcolor-message"></a>\_Mensagem GETTEXTBKCOLOR LVM

Recupera a cor da tela de fundo do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTextBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a cor do plano de fundo do texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





