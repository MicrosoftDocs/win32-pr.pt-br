---
title: TDM_SET_PROGRESS_BAR_RANGE mensagem (Commctrl.h)
description: Define os valores mínimo e máximo para a barra de progresso em uma caixa de diálogo de tarefa.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE controles Windows mensagem
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
ms.openlocfilehash: 54d94da64bd01b17addeb8f65def177e7e7e5d7daccbafb1629d1158f8c6636d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875906"
---
# <a name="tdm_set_progress_bar_range-message"></a>Mensagem TDM \_ SET \_ PROGRESS BAR \_ \_ RANGE

Define os valores mínimo e máximo para a barra de progresso em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o valor mínimo. Por padrão, o valor mínimo é zero. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o valor máximo. Por padrão, o valor máximo é 100.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna os valores mínimo e máximo anteriores, se bem-sucedido ou zero, caso contrário. A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o valor mínimo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o valor máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

