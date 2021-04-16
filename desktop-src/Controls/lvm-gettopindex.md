---
title: Mensagem de LVM_GETTOPINDEX (commctrl. h)
description: Recupera o índice do item visível superior no modo de exibição de lista ou de relatório. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTopIndex do ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- Controles de LVM_GETTOPINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811143"
---
# <a name="lvm_gettopindex-message"></a>\_Mensagem GETTOPINDEX LVM

Recupera o índice do item visível superior no modo de exibição de lista ou de relatório. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTopIndex do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item se for bem-sucedido. Retornará zero se o controle de exibição de lista estiver em um modo de exibição de ícone ou pequeno, ou se o controle de exibição de lista estiver no modo de exibição de detalhes com grupos habilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





