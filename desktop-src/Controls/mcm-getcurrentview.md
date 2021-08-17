---
title: MCM_GETCURRENTVIEW mensagem (Commctrl.h)
description: Obtém a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a \_ macro MonthCal GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW controles de Windows mensagem
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
ms.openlocfilehash: 50f7fce3c1a22ec14ec34e849bd2e3fc4634118b11613913da4e6fae0b9b7b51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319676"
---
# <a name="mcm_getcurrentview-message"></a>Mensagem MCM \_ GETCURRENTVIEW

Obtém a exibição atual do calendário. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ MonthCal GetCurrentView.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview)

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

## <a name="return-value"></a>Valor retornado

Exibição atual. Um dos valores a seguir.



| Código de retorno                                                                                  | Descrição              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**MCMV \_ MONTH**</dt> </dl>   | Exibição mensal.<br/> |
| <dl> <dt>**MCMV \_ YEAR**</dt> </dl>    | Exibição anual.<br/>  |
| <dl> <dt>**MCMV \_ DECADE**</dt> </dl>  | Exibição de década.<br/>  |
| <dl> <dt>**MCMV \_ CENTURY**</dt> </dl> | Exibição de século.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





