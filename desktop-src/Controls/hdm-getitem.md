---
title: Mensagem de HDM_GETITEM (commctrl. h)
description: Obtém informações sobre um item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetItem do cabeçalho.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- controles de Windows de mensagem de HDM_GETITEM
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 566f8b8e3bdf4e92abfb1fdd5874b8514814792e1d7aae169cc2aca4b2e8d101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436186"
---
# <a name="hdm_getitem-message"></a>\_Mensagem HDM GETITEM

Obtém informações sobre um item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item para o qual as informações serão recuperadas.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Quando a mensagem é enviada, o membro de **máscara** indica o tipo de informação que está sendo solicitada. Quando a mensagem retorna, os outros membros recebem as informações solicitadas. Se o membro de **máscara** especificar zero, a mensagem retornará **true** , mas não copiará nenhuma informação para a estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se o \_ sinalizador de texto HDI for definido no membro **Mask** da estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , o controle poderá alterar o membro **pszText** da estrutura para apontar para o novo texto em vez de preencher o buffer com o texto solicitado. Os aplicativos não devem pressupor que o texto sempre será colocado no buffer solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDM \_ GETITEMW** (Unicode) e **HDM \_ getitema** (ANSI)<br/>                   |



 

 





