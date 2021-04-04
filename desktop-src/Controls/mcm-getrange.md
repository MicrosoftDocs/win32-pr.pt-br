---
title: Mensagem de MCM_GETRANGE (commctrl. h)
description: Recupera as datas mínimas e máximas permitidas definidas para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetRange calendário mensal.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- Controles de MCM_GETRANGE de mensagens do Windows
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
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824765"
---
# <a name="mcm_getrange-message"></a>MCM \_ mensagem GETrange

Recupera as datas mínimas e máximas permitidas definidas para um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetRange calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá as informações de limite de data. O limite mínimo é definido em *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] recebe o limite máximo. Se qualquer elemento for definido como todos os zeros, nenhum limite correspondente será definido para o controle de calendário mensal. Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um **DWORD** que pode ser zero (nenhum limite é definido) ou uma combinação dos seguintes valores que especificam informações de limite:



| Código de retorno                                                                              | Descrição                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ Max**</dt> </dl> | Um limite máximo é definido para o controle; *lprgSysTimeArray* \[ 0 \] é válido e contém as informações de data aplicáveis. <br/> |
| <dl> <dt>**GDTR \_ mín.**</dt> </dl> | Um limite mínimo é definido para o controle; *lprgSysTimeArray* \[ 1 \] é válido e contém as informações de data aplicáveis. <br/> |



 

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

 

