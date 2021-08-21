---
title: TB_SETSTATE mensagem (Commctrl.h)
description: Define o estado do botão especificado em uma barra de ferramentas.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- TB_SETSTATE controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa9ee112e4bbbe9c64ceab6205d67ecd6ae9653df97be55991be38eb5d181d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167466"
---
# <a name="tb_setstate-message"></a>Mensagem TB \_ SETSTATE

Define o estado do botão especificado em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é uma combinação de valores listados em Estados [do Botão da Barra de Ferramentas](toolbar-button-states.md). O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

