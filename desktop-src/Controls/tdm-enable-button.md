---
title: Mensagem de TDM_ENABLE_BUTTON (commctrl. h)
description: Habilita ou desabilita um botão de ação em uma caixa de diálogo de tarefa.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- Controles de TDM_ENABLE_BUTTON de mensagens do Windows
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
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762747"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





