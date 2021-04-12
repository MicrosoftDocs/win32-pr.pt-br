---
title: Mensagem de MCM_GETCURRENTVIEW (commctrl. h)
description: Obtém a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- Controles de MCM_GETCURRENTVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455738"
---
# <a name="mcm_getcurrentview-message"></a>\_Mensagem MCM GETCURRENTVIEW

Obtém a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Exibição atual. Um dos valores a seguir.



| Código de retorno                                                                                  | Descrição              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**MCMV \_ mês**</dt> </dl>   | Exibição mensal.<br/> |
| <dl> <dt>**MCMV \_ ano**</dt> </dl>    | Exibição anual.<br/>  |
| <dl> <dt>**década de MCMV \_**</dt> </dl>  | Exibição da década.<br/>  |
| <dl> <dt>**\_século MCMV**</dt> </dl> | Exibição do século.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





