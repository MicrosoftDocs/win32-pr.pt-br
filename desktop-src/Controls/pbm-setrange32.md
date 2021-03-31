---
title: Mensagem de PBM_SETRANGE32 (commctrl. h)
description: Define os valores mínimo e máximo de uma barra de progresso para valores de 32 bits e redesenha a barra para refletir o novo intervalo.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- Controles de PBM_SETRANGE32 de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644907"
---
# <a name="pbm_setrange32-message"></a>Mensagem do SETRANGE32 do PBM \_

Define os valores mínimo e máximo de uma barra de progresso para valores de 32 bits e redesenha a barra para refletir o novo intervalo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de intervalo mínimo. Por padrão, o valor mínimo é zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor de intervalo máximo. Esse valor deve ser maior que *wParam*. Por padrão, o valor máximo é 100.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que contém o limite baixo de 16 bits anterior em seu [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o limite superior de 16 bits anterior em seu [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se os intervalos anteriores eram valores de 32 bits, o valor de retorno consiste em **LOWORD** s de ambos os limites de 32 bits.

## <a name="remarks"></a>Comentários

Para recuperar os valores inteiros de 32 bits altos e baixos, use a mensagem do [**PBM \_ GetRange**](pbm-getrange.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

