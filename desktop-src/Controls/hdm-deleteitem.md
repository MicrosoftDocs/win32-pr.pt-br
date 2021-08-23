---
title: Mensagem de HDM_DELETEITEM (commctrl. h)
description: Exclui um item de um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro DeleteItem do cabeçalho.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- controles de Windows de mensagem de HDM_DELETEITEM
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b0a48d769117ffd68f2ba2af9695fe7fce00031f297626ae48c111d4574dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697346"
---
# <a name="hdm_deleteitem-message"></a>\_Mensagem HDM DELETEITEM

Exclui um item de um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ DeleteItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um índice do item a ser excluído.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





