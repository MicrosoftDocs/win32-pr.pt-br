---
title: LVM_GETTOPINDEX mensagem (Commctrl.h)
description: Recupera o índice do item visível mais alto quando está na exibição de lista ou relatório. Você pode enviar essa mensagem explicitamente ou usando a \_ macro ListView GetTopIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX controles Windows mensagem
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
ms.openlocfilehash: 6434aa2c7382a4a4d54fc3a76edd5eb4b70ccae858b8d9fcf41547590a8bc69c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920036"
---
# <a name="lvm_gettopindex-message"></a>Mensagem GETTOPINDEX do LVM \_

Recupera o índice do item visível mais alto quando está na exibição de lista ou relatório. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ ListView GetTopIndex.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará o índice do item se for bem-sucedido. Retornará zero se o controle de exibição de lista estiver no ícone ou exibição de ícone pequeno ou se o controle de exibição de lista estiver na exibição de detalhes com grupos habilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





