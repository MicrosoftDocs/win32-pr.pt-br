---
title: TDM_CLICK_VERIFICATION mensagem (Commctrl.h)
description: Simula um clique da caixa de seleção de verificação de uma caixa de diálogo de tarefa, se ela existir.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION controles de Windows mensagem
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
ms.openlocfilehash: b3cda5e85b138225d69e159792cbe641122e91bf9602b3e0f5edafa419edc3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876086"
---
# <a name="tdm_click_verification-message"></a>Mensagem TDM \_ CLICK \_ VERIFICATION

Simula um clique da caixa de seleção de verificação de uma caixa de diálogo de tarefa, se ela existir.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

**TRUE** para definir o estado da caixa de seleção a ser marcada; **FALSE** para defini-lo como desmarcado.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

**TRUE** para definir o foco do teclado para a caixa de seleção; **FALSE caso** contrário, .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





