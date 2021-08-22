---
title: Mensagem de MCM_GETMONTHRANGE (commctrl. h)
description: Recupera informações de data (usando estruturas SYSTEMTIME) que representam os limites altos e baixos da exibição de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- controles de Windows de mensagem de MCM_GETMONTHRANGE
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc55f9732199f2e6e031248003c6dcad4abe8cb713182081666cfbee6a4ce50b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319576"
---
# <a name="mcm_getmonthrange-message"></a>\_Mensagem MCM GETMONTHRANGE

Recupera informações de data (usando estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ) que representam os limites altos e baixos da exibição de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica o escopo dos limites de intervalo a serem recuperados. Esse valor deve ser um dos seguintes:



| Valor                                                                                                                                                      | Significado                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**GMR \_ DAYSTATE**</dt> </dl> | Incluir meses anteriores e posteriores do intervalo visível que são exibidos apenas parcialmente. <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ visível**</dt> </dl>    | Inclua somente os meses que são totalmente exibidos. <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá os limites inferior e superior do escopo especificado por *wParam*. Os limites inferior e superior são colocados em *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] , respectivamente. Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor INT que representa o intervalo, em meses, estendido pelos dois limites retornados em *lParam*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vezes no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 

