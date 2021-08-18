---
title: Mensagem de LVM_SETITEMSTATE (commctrl. h)
description: Altera o estado de um item em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetItemState do ListView.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- controles de Windows de mensagem de LVM_SETITEMSTATE
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b7375ad7edb32459fe6029081ec0a872d3673c90003e34ca21cd795d3a79ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217411"
---
# <a name="lvm_setitemstate-message"></a>Mensagem do LVM \_ SETitemstate

Altera o estado de um item em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItemState do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item de exibição de lista. Se esse parâmetro for-1, a alteração de estado será aplicada a todos os itens.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . O membro **stateMask** especifica quais bits de estado alterar e o membro de **estado** contém os novos valores para esses bits. Os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se você enviar essa mensagem explicitamente, ela retornará **true** se for bem-sucedida ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O valor de estado de um item inclui um conjunto de sinalizadores de bits que indicam o estado do item. O valor de estado também pode incluir índices de lista de imagens que indicam a imagem de estado e a imagem de sobreposição do item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





