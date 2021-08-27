---
title: Mensagem de TDM_SET_PROGRESS_BAR_STATE (commctrl. h)
description: Define o estado da barra de progresso em uma caixa de diálogo de tarefa.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- controles de Windows de mensagem de TDM_SET_PROGRESS_BAR_STATE
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3be7432ac3a93af4f27fe9b06dced50fc6c77c0176c3bff7419cf15f2c73ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104526"
---
# <a name="tdm_set_progress_bar_state-message"></a>\_Mensagem de \_ estado da barra de progresso do conjunto TDM \_ \_

Define o estado da barra de progresso em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um **int** que especifica o estado da barra de progresso. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                   | Significado                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ normal**</dt> </dl> | Define a barra de progresso para o estado normal.<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST em \_ pausa**</dt> </dl>    | Define a barra de progresso para o estado em pausa.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**erro de PBST \_**</dt> </dl>    | Defina a barra de progresso para o estado de erro.<br/>   |



 

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame GetLastError.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





