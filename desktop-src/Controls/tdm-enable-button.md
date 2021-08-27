---
title: Mensagem de TDM_ENABLE_BUTTON (commctrl. h)
description: Habilita ou desabilita um botão de ação em uma caixa de diálogo de tarefa.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- controles de Windows de mensagem de TDM_ENABLE_BUTTON
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a76603f61f3e27dce8cf7c8f5504457ce5a29a787b3b1f6357c1c519c735854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104646"
---
# <a name="tdm_enable_button-message"></a>\_Mensagem de \_ botão habilitar TDM

Habilita ou desabilita um botão de ação em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um valor **int** que especifica a ID do botão de ação a ser habilitada ou desabilitada.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Especifica o estado do botão. Defina como 0 para desabilitar o botão; Defina como diferente de zero para habilitar o botão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





