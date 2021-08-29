---
title: LVM_DELETEITEM mensagem (Commctrl.h)
description: Remove um item de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteItem ListView.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- LVM_DELETEITEM controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88520e7d4f9d0d3ff22f90d7cea033b7674cfcbadbf55358f7ced8cc36c2399a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958415"
---
# <a name="lvm_deleteitem-message"></a>Mensagem LVM \_ DELETEITEM

Remove um item de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ DeleteItem ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item de exibição de lista a ser excluído.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





