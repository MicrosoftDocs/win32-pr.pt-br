---
title: Mensagem de TVM_SETHOT (commctrl. h)
description: Define o item ativo para um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetHot.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- controles de Windows de mensagem de TVM_SETHOT
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
ms.openlocfilehash: 87ca61fd0bd3e25f37229cd5cee54f9bbb59b3a5c7556ae745821a8dc4d595d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913946"
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

## <a name="return-value"></a>Valor retornado

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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SetHot TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





