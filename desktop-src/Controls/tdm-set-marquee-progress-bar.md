---
title: Mensagem de TDM_SET_MARQUEE_PROGRESS_BAR (commctrl. h)
description: Indica se a barra de progresso hospedada de uma caixa de diálogo de tarefa deve ser exibida no modo de letreiro.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- controles de Windows de mensagem de TDM_SET_MARQUEE_PROGRESS_BAR
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
ms.openlocfilehash: 13262339f7d87ea68755a38a49cc8c327706939d6b18025f350334dfdbe3dd4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104606"
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

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Para obter informações sobre o modo de letreiro, consulte [controle de barra de progresso](progress-bar-control.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





