---
title: Mensagem de TDM_ENABLE_RADIO_BUTTON (commctrl. h)
description: Habilita ou desabilita um botão de opção em uma caixa de diálogo de tarefa.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- controles de Windows de mensagem de TDM_ENABLE_RADIO_BUTTON
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493c6813f15baa3ad3b5ceb7050049f620010a9eed12d75d09b3c9f102aa62db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876066"
---
# <a name="tdm_enable_radio_button-message"></a>\_Mensagem do \_ botão de opção Habilitar TDM \_

Habilita ou desabilita um botão de opção em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um valor **int** que especifica a ID do botão de opção a ser habilitado ou desabilitado.

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



 

 





