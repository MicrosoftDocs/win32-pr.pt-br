---
title: Mensagem de TVM_HITTEST (commctrl. h)
description: Determina o local do ponto especificado em relação à área do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro HitTest do TreeView.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- Controles de TVM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009108"
---
# <a name="tvm_hittest-message"></a>\_Mensagem TVM HITTEST

Determina o local do ponto especificado em relação à área do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ HitTest do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) . Quando a mensagem é enviada, o membro **pt** especifica as coordenadas do ponto a ser testado. Quando a mensagem retornar, o membro **hItem** será o identificador para o item no ponto especificado ou **NULL** se nenhum item ocupar o ponto. Além disso, quando a mensagem retorna, o membro **flags** é um valor de teste de clique que indica o local do ponto especificado. Para obter uma lista de valores de teste de clique, consulte a descrição da estrutura **TVHITTESTINFO** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o item de exibição de árvore que ocupa o ponto especificado ou **nulo** se nenhum item ocupar o ponto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





