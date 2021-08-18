---
title: Mensagem de LVM_INSERTCOLUMN (commctrl. h)
description: Insere uma nova coluna em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro InsertColumn do ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- controles de Windows de mensagem de LVM_INSERTCOLUMN
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c2316ed2a74c82cd4530eff2d71d4771f4042b903c7ee17fc62886009ed5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019234"
---
# <a name="lvm_insertcolumn-message"></a>\_Mensagem INSERTCOLUMN LVM

Insere uma nova coluna em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ InsertColumn do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da nova coluna.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contém os atributos da nova coluna.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice da nova coluna se for bem-sucedido ou-1 caso contrário.

## <a name="remarks"></a>Comentários

As colunas são visíveis somente na exibição de relatório (detalhes).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





