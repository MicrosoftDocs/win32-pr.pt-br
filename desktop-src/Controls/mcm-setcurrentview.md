---
title: Mensagem de MCM_SETCURRENTVIEW (commctrl. h)
description: Define a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- Controles de MCM_SETCURRENTVIEW de mensagens do Windows
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
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919085"
---
# <a name="mcm_setcurrentview-message"></a>\_Mensagem MCM SETCURRENTVIEW

Define a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .

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
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**MCMV \_ mês**</dt> </dl>       | Exibição mensal.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**MCMV \_ ano**</dt> </dl>          | Exibição anual.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**década de MCMV \_**</dt> </dl>    | Exibição da década.<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**\_século MCMV**</dt> </dl> | Exibição do século.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





