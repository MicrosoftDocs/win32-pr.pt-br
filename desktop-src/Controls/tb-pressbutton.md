---
title: TB_PRESSBUTTON mensagem (Commctrl.h)
description: Pressiona ou libera o botão especificado em uma barra de ferramentas.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- TB_PRESSBUTTON controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c72bd3e58b06510463fcfb872060d7fcbb529ce3e5a96376ae8cb25e142d9e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168006"
---
# <a name="tb_pressbutton-message"></a>Mensagem \_ PRESSBUTTON de TB

Pressiona ou libera o botão especificado em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão a ser pressionado ou liberado.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é **um BOOL** que indica se o botão especificado deve ser pressionado ou liberado. Se **TRUE**, o botão será pressionado. Se **FALSE**, o botão será liberado.

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



 

