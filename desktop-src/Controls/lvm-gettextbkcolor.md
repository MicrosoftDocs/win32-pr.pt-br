---
title: Mensagem de LVM_GETTEXTBKCOLOR (commctrl. h)
description: Recupera a cor da tela de fundo do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTextBkColor do ListView.
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- controles de Windows de mensagem de LVM_GETTEXTBKCOLOR
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
ms.openlocfilehash: 88bc7d22766f2d1bed304c5e9780faf05808513312b744ae54bc2d6cfab6dffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958255"
---
# <a name="lvm_gettextbkcolor-message"></a>\_Mensagem GETTEXTBKCOLOR LVM

Recupera a cor da tela de fundo do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTextBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a cor do plano de fundo do texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





