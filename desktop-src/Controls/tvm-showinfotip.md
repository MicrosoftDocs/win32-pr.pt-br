---
title: Mensagem de TVM_SHOWINFOTIP (commctrl. h)
description: Mostra o InfoTip de um item especificado em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ ShowInfoTip.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- Controles de TVM_SHOWINFOTIP de mensagens do Windows
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
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824803"
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

## <a name="return-value"></a>Retornar valor

Retorna zero.

## <a name="remarks"></a>Comentários

A maioria dos aplicativos não usa essa mensagem. Infotips são mostrados automaticamente. Para obter mais informações, consulte usando Tree-View Infotips na visão geral [sobre controles About Tree-View](tree-view-controls.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





