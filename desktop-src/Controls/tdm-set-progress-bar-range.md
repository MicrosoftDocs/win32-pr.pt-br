---
title: Mensagem de TDM_SET_PROGRESS_BAR_RANGE (commctrl. h)
description: Define os valores mínimo e máximo para a barra de progresso em uma caixa de diálogo de tarefa.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- Controles de TDM_SET_PROGRESS_BAR_RANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824804"
---
# <a name="tdm_set_progress_bar_range-message"></a>\_Mensagem de \_ intervalo da barra de progresso do conjunto TDM \_ \_

Define os valores mínimo e máximo para a barra de progresso em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor mínimo. Por padrão, o valor mínimo é zero. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor máximo. Por padrão, o valor máximo é 100.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna os valores mínimo e máximo anteriores, se bem-sucedido, ou zero caso contrário. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o valor mínimo e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o valor máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

