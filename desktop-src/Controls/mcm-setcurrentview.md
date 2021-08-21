---
title: MCM_SETCURRENTVIEW mensagem (Commctrl.h)
description: Define a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro MonthCal \_ SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW controles de Windows mensagem
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cf7206fb7e778c0ab7d28ee8947b9327e8cc98bd8ae8c9063213814676a77e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019034"
---
# <a name="mcm_setcurrentview-message"></a>Mensagem MCM \_ SETCURRENTVIEW

Define a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro [**MonthCal \_ SetCurrentView.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nova exibição. Uma das constantes a seguir.



| Valor                                                                                                                                                      | Significado                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**MCMV \_ MONTH**</dt> </dl>       | Exibição mensal.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**MCMV \_ YEAR**</dt> </dl>          | Exibição anual.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**MCMV \_ DECADE**</dt> </dl>    | Exibição de década.<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**MCMV \_ CENTURY**</dt> </dl> | Exibição de século.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





