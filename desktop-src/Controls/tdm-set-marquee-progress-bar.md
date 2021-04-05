---
title: Mensagem de TDM_SET_MARQUEE_PROGRESS_BAR (commctrl. h)
description: Indica se a barra de progresso hospedada de uma caixa de diálogo de tarefa deve ser exibida no modo de letreiro.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- Controles de TDM_SET_MARQUEE_PROGRESS_BAR de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086319"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>\_Mensagem da \_ barra de \_ progresso do letreiro de conjunto de TDM \_

Indica se a barra de progresso hospedada de uma caixa de diálogo de tarefa deve ser exibida no modo de letreiro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um **bool** que indica se a barra de progresso deve ser mostrada no modo de letreiro. Um valor **true** ativa o modo de letreiro e um valor de **false** desativa o modo de letreiro.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Para obter informações sobre o modo de letreiro, consulte [controle de barra de progresso](progress-bar-control.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





