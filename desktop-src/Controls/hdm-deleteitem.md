---
title: Mensagem de HDM_DELETEITEM (commctrl. h)
description: Exclui um item de um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro DeleteItem do cabeçalho.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- Controles de HDM_DELETEITEM de mensagens do Windows
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
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009525"
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

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





