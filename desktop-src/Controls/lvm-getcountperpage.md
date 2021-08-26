---
title: Mensagem de LVM_GETCOUNTPERPAGE (commctrl. h)
description: Calcula o número de itens que podem se ajustar verticalmente na área visível de um controle de exibição de lista no modo de exibição de lista ou de relatório. Somente os itens totalmente visíveis são contados. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetCountPerPage do ListView.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- controles de Windows de mensagem de LVM_GETCOUNTPERPAGE
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
ms.openlocfilehash: deb5e7acf0c3db4add2d986a1821b9a76ae30fc1aec0af369e48e35e2a424f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968336"
---
# <a name="lvm_getcountperpage-message"></a>\_Mensagem GETCOUNTPERPAGE LVM

Calcula o número de itens que podem se ajustar verticalmente na área visível de um controle de exibição de lista no modo de exibição de lista ou de relatório. Somente os itens totalmente visíveis são contados. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetCountPerPage do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de itens totalmente visíveis se for bem-sucedido. Se a exibição atual for ícone ou exibição de ícone pequeno, o valor de retorno será o número total de itens no controle de exibição de lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





