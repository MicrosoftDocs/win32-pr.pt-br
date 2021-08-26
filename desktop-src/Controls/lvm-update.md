---
title: Mensagem de LVM_UPDATE (commctrl. h)
description: Atualiza um item de exibição de lista. Se o controle de exibição de lista tiver o \_ estilo de AUTOORGANIZAR LVS, essa macro fará com que o controle de exibição de lista seja organizado. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ atualização de ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- controles de Windows de mensagem de LVM_UPDATE
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
ms.openlocfilehash: ff9067d6eb80c5db7880ee9331a04e9259e9c841ccfe7dd80158a2afbcd06c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915226"
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

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





