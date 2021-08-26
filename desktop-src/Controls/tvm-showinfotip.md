---
title: Mensagem de TVM_SHOWINFOTIP (commctrl. h)
description: Mostra o InfoTip de um item especificado em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ ShowInfoTip.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- controles de Windows de mensagem de TVM_SHOWINFOTIP
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1cf61511e8c9e69c42d89f99fc4ddae90de78701e5e75170ff1b793671120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913916"
---
# <a name="tvm_showinfotip-message"></a>\_Mensagem TVM SHOWINFOTIP

Mostra o InfoTip de um item especificado em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Identificador para o item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna zero.

## <a name="remarks"></a>Comentários

A maioria dos aplicativos não usa essa mensagem. Infotips são mostrados automaticamente. Para obter mais informações, consulte usando Tree-View Infotips na visão geral [sobre controles About Tree-View](tree-view-controls.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





