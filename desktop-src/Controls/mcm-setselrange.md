---
title: Mensagem de MCM_SETSELRANGE (commctrl. h)
description: Define a seleção de um controle de calendário de mês para um determinado intervalo de datas. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetSelRange.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- Controles de MCM_SETSELRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008929"
---
# <a name="mcm_setselrange-message"></a>\_Mensagem MCM SETSELRANGE

Define a seleção de um controle de calendário de mês para um determinado intervalo de datas. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contêm informações de data que representam os limites de seleção. A primeira data selecionada deve ser especificada em *lpSysTimeArray* \[ 0 \] , e a última data selecionada deve ser especificada em *lpSysTimeArray* \[ 1 \] .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro. Esta mensagem falhará se for aplicada a um controle de calendário de mês que não usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .

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

 

