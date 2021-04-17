---
title: Mensagem de MCM_SETRANGE (commctrl. h)
description: Define as datas mínimas e máximas permitidas para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetRange calendário mensal.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- Controles de MCM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762751"
---
# <a name="mcm_setrange-message"></a>\_Mensagem SETRANGE MCM

Define as datas mínimas e máximas permitidas para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetRange calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valores de sinalizador que especificam quais limites de data estão sendo definidos. Esse valor deve ser um ou ambos os seguintes:



| Valor                                                                                                                                          | Significado                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ Max**</dt> </dl> | A data máxima permitida está sendo definida. A estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em *lpSysTimeArray* \[ 1 \] deve conter informações de data. <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ mín.**</dt> </dl> | A data mínima permitida está sendo definida. A estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em *lpSysTimeArray* \[ 0 \] deve conter informações de data. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contêm os limites de data. O limite máximo deve estar em *lpSysTimeArray* \[ 1 \] se GDTR \_ Max for especificado e *lpSysTimeArray* \[ 0 \] deve conter o limite mínimo se GDTR \_ min for especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vezes no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 

