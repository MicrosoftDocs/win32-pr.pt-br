---
title: Mensagem de UDM_GETRANGE (commctrl. h)
description: Recupera as posições mínima e máxima (intervalo) para um controle acima-abaixo.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- controles de Windows de mensagem de UDM_GETRANGE
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13811f383886e0e4985eb3f2f5093eec53cb0745349a36ca133fa3de9656773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408096"
---
# <a name="udm_getrange-message"></a>Mensagem do UDM \_ GETrange

Recupera as posições mínima e máxima (intervalo) para um controle acima-abaixo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um valor de 32 bits que contém as posições mínima e máxima. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é a posição máxima do controle e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é a posição mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

