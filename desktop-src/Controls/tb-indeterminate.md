---
title: TB_INDETERMINATE mensagem (Commctrl.h)
description: Define ou limpa o estado indeterminado do botão especificado em uma barra de ferramentas.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90845f269d0af1e690d5ddeb02f2a8ec2a2f63ff4f698f1dd0f3e2729d98b72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078260"
---
# <a name="tb_indeterminate-message"></a>Mensagem \_ TB INDETERMINADA

Define ou limpa o estado indeterminado do botão especificado em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão cujo estado indeterminado deve ser definido ou limpo.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é **um BOOL** que indica se deve-se definir ou limpar o estado indeterminado. Se **TRUE**, o estado indeterminado será definido. Se **FALSE**, o estado será limpo.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

