---
title: TVM_GETVISIBLECOUNT mensagem (Commctrl.h)
description: Obtém o número de itens que podem ser totalmente visíveis na janela do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetVisibleCount.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT controles Windows mensagem
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07604eed3d3ece140d33bb9c612a2f898f6de02785f2c9916332de60358693fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698654"
---
# <a name="tvm_getvisiblecount-message"></a>Mensagem TVM \_ GETVISIBLECOUNT

Obtém o número de itens que podem ser totalmente visíveis na janela do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetVisibleCount.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de itens que podem ser totalmente visíveis na janela do cliente do controle de exibição de árvore.

## <a name="remarks"></a>Comentários

O número de itens que podem ser totalmente visíveis pode ser maior que o número de itens no controle . O controle calcula esse valor dividindo a altura da janela do cliente pela altura de um item.

Observe que o valor de retorno é o número de itens que podem ser *totalmente visíveis.* Se você puder ver todos os 20 itens e parte de mais um item, o valor de retorno será 20.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





