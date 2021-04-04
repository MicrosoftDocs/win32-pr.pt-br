---
title: Mensagem de TDM_CLICK_VERIFICATION (commctrl. h)
description: Simula um clique da caixa de seleção de verificação de uma caixa de diálogo de tarefa, se ela existir.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- Controles de TDM_CLICK_VERIFICATION de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085149"
---
# <a name="tdm_click_verification-message"></a>Mensagem de verificação de \_ clique de TDM \_

Simula um clique da caixa de seleção de verificação de uma caixa de diálogo de tarefa, se ela existir.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

**True** para definir o estado da caixa de seleção como marcada; **False** para defini-lo como desmarcado.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

**True** para definir o foco do teclado para a caixa de seleção; Caso contrário, **false** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





