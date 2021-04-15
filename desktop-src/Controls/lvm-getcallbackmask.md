---
title: Mensagem de LVM_GETCALLBACKMASK (commctrl. h)
description: Obtém a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetCallbackMask do ListView.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- Controles de LVM_GETCALLBACKMASK de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454633"
---
# <a name="lvm_getcallbackmask-message"></a>\_Mensagem GETCALLBACKMASK LVM

Obtém a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetCallbackMask do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a máscara de retorno de chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





