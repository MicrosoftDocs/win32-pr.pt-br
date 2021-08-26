---
title: LVM_GETCALLBACKMASK mensagem (Commctrl.h)
description: Obtém a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetCallbackMask listView.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- LVM_GETCALLBACKMASK controles de Windows mensagem
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
ms.openlocfilehash: 58cbfec76df9418c2bc94e0083928f28e462188383a203237dd03f3f175c74b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920226"
---
# <a name="lvm_getcallbackmask-message"></a>Mensagem GETCALLBACKMASK do LVM \_

Obtém a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetCallbackMask listView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a máscara de retorno de chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





