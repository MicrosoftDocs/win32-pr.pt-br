---
title: TCM_DELETEITEM mensagem (Commctrl.h)
description: Remove um item de um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteItem TabCtrl.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM controles Windows mensagem
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc9e90ab63e34545628019cd9dcde74c7b4e953fb6ee0b9eed138151129e7b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077870"
---
# <a name="tcm_deleteitem-message"></a>Mensagem TCM \_ DELETEITEM

Remove um item de um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ DeleteItem TabCtrl.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item a ser excluído.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





