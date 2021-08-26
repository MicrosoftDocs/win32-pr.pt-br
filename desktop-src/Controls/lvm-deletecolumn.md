---
title: LVM_DELETECOLUMN mensagem (Commctrl.h)
description: Remove uma coluna de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteColumn listView.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN controles Windows mensagem
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
ms.openlocfilehash: 039ab92028d23a75518237bc6e9723f051f2f6f2de8732e40f2086d027a61873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920316"
---
# <a name="lvm_deletecolumn-message"></a>Mensagem LVM \_ DELETECOLUMN

Remove uma coluna de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ DeleteColumn listView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice da coluna a ser excluído.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

A exclusão da coluna zero de um controle de exibição de lista só tem suporte ComCtl32.dll versão 6 e posteriores. A versão 5 também dá suporte à exclusão da coluna zero, mas somente depois de usar [**CCM \_ SETVERSION**](ccm-setversion.md) para definir a versão como 5 ou posterior. Em versões anteriores à versão 5, se você deve excluir a coluna zero, insira uma coluna fiada de comprimento zero zero e exclua a coluna 1 e superior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





