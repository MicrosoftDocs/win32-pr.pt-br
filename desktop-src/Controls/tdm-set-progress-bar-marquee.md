---
title: TDM_SET_PROGRESS_BAR_MARQUEE mensagem (Commctrl.h)
description: Inicia e interrompe a exibição do letreiro da barra de progresso em uma caixa de diálogo de tarefa e define a velocidade do letreiro.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE controles de Windows mensagem
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
ms.openlocfilehash: 5b92816b70e683b9f58e0de2247b2710da38bee891caa39d9026fc342168c6be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060646"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>Mensagem TDM \_ SET \_ PROGRESS BAR \_ \_ MARQUEE

Inicia e interrompe a exibição do letreiro da barra de progresso em uma caixa de diálogo de tarefa e define a velocidade do letreiro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

Um **BOOL** que indica se o letreiro deve ser exibido ou desligado. Use **TRUE** para ativar a exibição do letreiro ou **FALSE** para a desligar.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

Um **UINT que** especifica o tempo, em milissegundos, entre as atualizações de animação do letreiro. Se esse parâmetro for zero, a animação de letreiro será atualizada a cada 30 milissegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Para obter informações sobre o modo de letreiro, consulte [Controle de barra de progresso](progress-bar-control.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





