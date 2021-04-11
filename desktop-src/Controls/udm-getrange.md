---
title: Mensagem de UDM_GETRANGE (commctrl. h)
description: Recupera as posições mínima e máxima (intervalo) para um controle acima-abaixo.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- Controles de UDM_GETRANGE de mensagens do Windows
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
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163627"
---
# <a name="udm_getrange-message"></a>Mensagem do UDM \_ GETrange

Recupera as posições mínima e máxima (intervalo) para um controle acima-abaixo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um valor de 32 bits que contém as posições mínima e máxima. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é a posição máxima do controle e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é a posição mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

