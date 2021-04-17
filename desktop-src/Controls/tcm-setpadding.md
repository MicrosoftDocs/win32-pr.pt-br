---
title: Mensagem de TCM_SETPADDING (commctrl. h)
description: Define a quantidade de espaço (preenchimento) em volta do ícone e do rótulo de cada guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setpadding TabCtrl.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- Controles de TCM_SETPADDING de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754370"
---
# <a name="tcm_setpadding-message"></a>\_Mensagem de AUTOpreenchimento do TCM

Define a quantidade de espaço (preenchimento) em volta do ícone e do rótulo de cada guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setpadding TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um valor **int** que especifica a quantidade de preenchimento horizontal, em pixels. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um valor **int** que especifica a quantidade de preenchimento vertical, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

