---
title: Mensagem de LVM_GETBKCOLOR (commctrl. h)
description: Obtém a cor da tela de fundo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetBkColor do ListView.
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- controles de Windows de mensagem de LVM_GETBKCOLOR
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6c768b9d27b3e8eda2f9b46988e261f82bba28ed9c70647420e6bfb36fdc29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920266"
---
# <a name="lvm_getbkcolor-message"></a>\_Mensagem GETBKCOLOR LVM

Obtém a cor da tela de fundo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a cor da tela de fundo do controle de exibição de lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





