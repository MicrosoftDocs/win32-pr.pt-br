---
title: Mensagem de HDM_GETITEMCOUNT (commctrl. h)
description: Obtém uma contagem dos itens em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetItemCount do cabeçalho.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- Controles de HDM_GETITEMCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085824"
---
# <a name="hdm_getitemcount-message"></a>\_Mensagem HDM GETitemcount

Obtém uma contagem dos itens em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetItemCount do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de itens, se for bem-sucedido, ou-1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





