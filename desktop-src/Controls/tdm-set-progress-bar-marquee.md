---
title: Mensagem de TDM_SET_PROGRESS_BAR_MARQUEE (commctrl. h)
description: Inicia e interrompe a exibição de letreiro da barra de progresso em uma caixa de diálogo de tarefa e define a velocidade do letreiro.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- Controles de TDM_SET_PROGRESS_BAR_MARQUEE de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009704"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>\_Mensagem de \_ letreiro da barra de progresso \_ \_ do TDM Set

Inicia e interrompe a exibição de letreiro da barra de progresso em uma caixa de diálogo de tarefa e define a velocidade do letreiro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um **bool** que indica se a exibição do letreiror deve ser ativada ou desativada. Use **true** para ativar a exibição do letreiro ou **false** para desativá-la.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Um **uint** que especifica o tempo, em milissegundos, entre as atualizações de animação do letreiro digital. Se esse parâmetro for zero, a animação do letreiro digital será atualizada a cada 30 milissegundos.

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



 

 





