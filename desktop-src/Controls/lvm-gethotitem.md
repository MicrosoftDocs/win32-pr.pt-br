---
title: Mensagem de LVM_GETHOTITEM (commctrl. h)
description: Recupera o índice do item ativo. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetHotItem do ListView.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- controles de Windows de mensagem de LVM_GETHOTITEM
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 743bd7a80a58bec41fa5a75f24b0e333ab33ad152909adb6ea69a9c4ca0fd78b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958395"
---
# <a name="lvm_gethotitem-message"></a>\_Mensagem GETHOTITEM LVM

Recupera o índice do item ativo. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetHotItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do item que está quente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





