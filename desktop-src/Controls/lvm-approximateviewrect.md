---
title: Mensagem de LVM_APPROXIMATEVIEWRECT (commctrl. h)
description: Calcula a largura aproximada e a altura necessárias para exibir um determinado número de itens. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ApproximateViewRect do ListView.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- controles de Windows de mensagem de LVM_APPROXIMATEVIEWRECT
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fcbb5476f28debd28116a52123bd01b8030c8b0a0c9c52e6598c864caed021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047056"
---
# <a name="lvm_approximateviewrect-message"></a>\_Mensagem APPROXIMATEVIEWRECT LVM

Calcula a largura aproximada e a altura necessárias para exibir um determinado número de itens. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ ApproximateViewRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de itens a serem exibidos no controle. Se esse parâmetro for definido como-1, a mensagem usará o número total de itens no controle.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é a dimensão x proposta do controle, em pixels. Esse parâmetro pode ser definido como-1 para permitir que a mensagem use o valor de largura atual.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é a dimensão y proposta do controle, em pixels. Esse parâmetro pode ser definido como-1 para permitir que a mensagem use o valor da altura atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **DWORD** que contém a largura aproximada (no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) e a altura (no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) necessárias para exibir os itens, em pixels.

## <a name="remarks"></a>Comentários

Definir o tamanho do controle de exibição de lista com base nas dimensões fornecidas por essa mensagem pode otimizar o redesenho e a redução da cintilação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

