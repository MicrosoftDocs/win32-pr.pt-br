---
title: Mensagem de TVM_SETHOT (commctrl. h)
description: Define o item ativo para um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetHot.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- Controles de TVM_SETHOT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919017"
---
# <a name="tvm_sethot-message"></a>\_Mensagem TVM SETHOT

\[Destinado ao uso interno; Não recomendado para uso em aplicativos. Essa mensagem pode não ter suporte em versões futuras do Windows.\]

Define o item ativo para um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o novo item ativo. Se esse valor for **nulo**, o controle de exibição de árvore será definido como sem item ativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="security-considerations"></a>Considerações de segurança

O uso dessa mensagem pode comprometer a segurança do seu programa.

## <a name="remarks"></a>Comentários

O *item ativo* é o item que o mouse está focalizando. Essa mensagem faz com que um item pareça ser o item ativo, mesmo que o mouse não esteja passando por ele.

Essa mensagem não terá efeito visível se o estilo de [**\_ TRACKSELECT de TVs**](tree-view-control-window-styles.md) não estiver definido.

Se tiver sucesso, essa mensagem fará com que o item ativo seja redesenhado.

Essa mensagem será ignorada se *lParam* for **NULL** e o controle de exibição de árvore estiver acompanhando o mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SetHot TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





