---
title: Mensagem de LVM_SCROLL (commctrl. h)
description: Rola o conteúdo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ rolagem de ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- Controles de LVM_SCROLL de mensagens do Windows
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
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455427"
---
# <a name="lvm_scroll-message"></a>\_Mensagem de rolagem LVM

Rola o conteúdo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ rolagem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do tipo **int** que especifica a quantidade de rolagem horizontal, em pixels, relativa à posição atual do conteúdo da exibição de lista. Se o controle de exibição de lista estiver no modo de exibição de lista, esse valor será arredondado para o número mais próximo de pixels que formam uma coluna inteira.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor do tipo **int** que especifica a quantidade de rolagem vertical, em pixels, relativa à posição atual do conteúdo da exibição de lista.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Quando o controle de exibição de lista está no modo de exibição de relatório, o controle só pode ser rolado verticalmente em incrementos de linha inteira. Portanto, o parâmetro *lParam* será arredondado para o número mais próximo de pixels que formam um incremento de linha inteiro. Por exemplo, se a altura de uma linha for de 16 pixels e 8 for passada para *lParam*, a lista será rolada por 16 pixels (1 linha). Se 7 for passado para *lParam*, a lista será rolada em 0 pixels (0 linhas).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





