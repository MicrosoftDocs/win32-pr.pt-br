---
title: TVM_HITTEST mensagem (Commctrl.h)
description: Determina o local do ponto especificado em relação à área do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ HitTest.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST controles de Windows mensagem
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
ms.openlocfilehash: e564b6d82c04c0d007784aac39284db13b3776267d524d2f615353ede50eb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060146"
---
# <a name="tvm_hittest-message"></a>Mensagem TVM \_ HITTEST

Determina o local do ponto especificado em relação à área do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TVHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) Quando a mensagem é enviada, o **membro pt** especifica as coordenadas do ponto a ser testado. Quando a mensagem retorna, o membro **hItem** é o alçador para o item no ponto especificado ou **NULL** se nenhum item ocupa o ponto. Além disso, quando a mensagem retorna, o membro **de sinalizadores** é um valor de teste de acerto que indica o local do ponto especificado. Para ver uma lista de valores de teste de acerto, consulte a descrição da estrutura **TVHITTESTINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para o item de exibição de árvore que ocupa o ponto especificado ou **NULL** se nenhum item ocupa o ponto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





