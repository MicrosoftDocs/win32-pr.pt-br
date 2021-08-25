---
title: TCM_SETPADDING mensagem (Commctrl.h)
description: Define a quantidade de espaço (preenchimento) em torno do ícone e do rótulo de cada guia em um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetPadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING controles de Windows mensagem
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
ms.openlocfilehash: 969ae3c7c240c38a6643682321c14e5744f2d2c2eec188004d1c3b2e6f2b3835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876236"
---
# <a name="tcm_setpadding-message"></a>Mensagem TCM \_ SETPADDING

Define a quantidade de espaço (preenchimento) em torno do ícone e do rótulo de cada guia em um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a [**macro TabCtrl \_ SetPadding.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **valor INT** que especifica a quantidade de preenchimento horizontal, em pixels. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **valor INT** que especifica a quantidade de preenchimento vertical, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

