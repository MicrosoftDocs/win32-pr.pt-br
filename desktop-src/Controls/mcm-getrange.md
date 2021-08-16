---
title: MCM_GETRANGE mensagem (Commctrl.h)
description: Recupera as datas mínimas e máximas permitidas definidas para um controle de calendário de mês. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetRange MonthCal.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE controles de Windows mensagem
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f8b9d5a485b12caf720afe518a2fc5499e55eba07c90c2fde1bb34eea2404b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830390"
---
# <a name="mcm_getrange-message"></a>Mensagem \_ GETRANGE do MCM

Recupera as datas mínimas e máximas permitidas definidas para um controle de calendário de mês. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetRange MonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de dois elementos de [**estruturas SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá as informações de limite de data. O limite mínimo é definido *em lprgSysTimeArray* \[ 0 e \] *lprgSysTimeArray* 1 recebe \[ o limite \] máximo. Se um dos elementos for definido como todos os zeros, nenhum limite correspondente será definido para o controle de calendário do mês. Esse parâmetro deve ser um endereço válido e não pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **DWORD** que pode ser zero (nenhum limite é definido) ou uma combinação dos seguintes valores que especificam informações de limite:



| Código de retorno                                                                              | Descrição                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ MAX**</dt> </dl> | Um limite máximo é definido para o controle ; *lprgSysTimeArray* \[ 0 \] é válido e contém as informações de data aplicáveis. <br/> |
| <dl> <dt>**GDTR \_ MIN**</dt> </dl> | Um limite mínimo é definido para o controle ; *lprgSysTimeArray* \[ 1 \] é válido e contém as informações de data aplicáveis. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Horas no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 

