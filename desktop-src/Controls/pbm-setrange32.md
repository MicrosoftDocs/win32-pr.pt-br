---
title: PBM_SETRANGE32 mensagem (Commctrl.h)
description: Define os valores mínimo e máximo de uma barra de progresso como valores de 32 bits e redesenha a barra para refletir o novo intervalo.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- PBM_SETRANGE32 controles de Windows mensagem
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
ms.openlocfilehash: f8e29022b4b3cb1c42c8e661e8366324ac10ae9853f104f31722dae8852edf71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169852"
---
# <a name="pbm_setrange32-message"></a>Mensagem PBM \_ SETRANGE32

Define os valores mínimo e máximo de uma barra de progresso como valores de 32 bits e redesenha a barra para refletir o novo intervalo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor mínimo do intervalo. Por padrão, o valor mínimo é zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor máximo do intervalo. Esse valor deve ser maior que *wParam.* Por padrão, o valor máximo é 100.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor DWORD** que contém o limite baixo de 16 bits anterior em seu [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o limite superior de 16 bits anterior em [**seu HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se os intervalos anteriores fossem valores de 32 bits, o valor de retorno consiste em **LOWORD** s de ambos os limites de 32 bits.

## <a name="remarks"></a>Comentários

Para recuperar todos os valores altos e baixos de 32 bits, use a [**mensagem \_ PBM GETRANGE.**](pbm-getrange.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

