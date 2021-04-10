---
title: Mensagem de LVM_GETCOUNTPERPAGE (commctrl. h)
description: Calcula o número de itens que podem se ajustar verticalmente na área visível de um controle de exibição de lista no modo de exibição de lista ou de relatório. Somente os itens totalmente visíveis são contados. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetCountPerPage do ListView.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- Controles de LVM_GETCOUNTPERPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008866"
---
# <a name="lvm_getcountperpage-message"></a>\_Mensagem GETCOUNTPERPAGE LVM

Calcula o número de itens que podem se ajustar verticalmente na área visível de um controle de exibição de lista no modo de exibição de lista ou de relatório. Somente os itens totalmente visíveis são contados. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetCountPerPage do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de itens totalmente visíveis se for bem-sucedido. Se a exibição atual for ícone ou exibição de ícone pequeno, o valor de retorno será o número total de itens no controle de exibição de lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





