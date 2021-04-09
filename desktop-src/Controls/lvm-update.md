---
title: Mensagem de LVM_UPDATE (commctrl. h)
description: Atualiza um item de exibição de lista. Se o controle de exibição de lista tiver o \_ estilo de AUTOORGANIZAR LVS, essa macro fará com que o controle de exibição de lista seja organizado. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ atualização de ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- Controles de LVM_UPDATE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824194"
---
# <a name="lvm_update-message"></a>Mensagem de atualização do LVM \_

Atualiza um item de exibição de lista. Se o controle de exibição de lista tiver o estilo de [**\_ AutoOrganizar LVS**](list-view-window-styles.md) , essa macro fará com que o controle de exibição de lista seja organizado. Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ atualização de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item a ser atualizado.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





