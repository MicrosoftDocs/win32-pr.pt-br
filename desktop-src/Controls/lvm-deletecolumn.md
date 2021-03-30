---
title: Mensagem de LVM_DELETECOLUMN (commctrl. h)
description: Remove uma coluna de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteColumn do ListView.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- Controles de LVM_DELETECOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644267"
---
# <a name="lvm_deletecolumn-message"></a>\_Mensagem DELETECOLUMN LVM

Remove uma coluna de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ DeleteColumn do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice da coluna a ser excluído.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A exclusão de coluna zero de um controle de exibição de lista tem suporte apenas no ComCtl32.dll versão 6 e posterior. A versão 5 também dá suporte à exclusão de coluna zero, mas somente depois de usar [**CCM \_ SetVersion**](ccm-setversion.md) para definir a versão como 5 ou posterior. Em versões anteriores à versão 5, se você precisar excluir a coluna zero, insira uma coluna fictícia de comprimento zero zero e exclua a coluna um e acima.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





