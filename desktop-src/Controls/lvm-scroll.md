---
title: LVM_SCROLL mensagem (Commctrl.h)
description: Rola o conteúdo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro Rolagem de \_ ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 604ef35b6d7e62e626aa7cbee32c1563224794781275c470a1b3cd1727b926bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019224"
---
# <a name="lvm_scroll-message"></a>Mensagem LVM \_ SCROLL

Rola o conteúdo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**Rolagem de \_ ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do tipo **int** que especifica a quantidade de rolagem horizontal, em pixels, em relação à posição atual do conteúdo da exibição de lista. Se o controle de exibição de lista estiver na exibição de lista, esse valor será arredondado para cima até o número mais próximo de pixels que formam uma coluna inteira.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor do tipo **int** que especifica a quantidade de rolagem vertical, em pixels, em relação à posição atual do conteúdo da exibição de lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se for bem-sucedido; caso contrário, **FALSE.**

## <a name="remarks"></a>Comentários

Quando o controle de exibição de lista está na exibição de relatório, o controle só pode ser rolado verticalmente em incrementos de linha inteira. Portanto, o *parâmetro lParam* será arredondado para o número mais próximo de pixels que formam um incremento de linha inteira. Por exemplo, se a altura de uma linha for de 16 pixels e 8 for passada para *lParam*, a lista será rolada por 16 pixels (1 linha). Se 7 for passado para *lParam*, a lista será rolada 0 pixels (0 linhas).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





