---
title: Mensagem de BCM_SETSHIELD (commctrl. h)
description: Define o estado de elevação necessária para um link de botão ou comando especificado para exibir um ícone com privilégios elevados. Envie essa mensagem explicitamente ou usando o botão \_ SetElevationRequiredState macro.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- controles de Windows de mensagem de BCM_SETSHIELD
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ab7ab495e713d9f2c8d58c6723489f0099a7c2cba9df93d4f08870d521a0cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921486"
---
# <a name="bcm_setshield-message"></a>\_Mensagem de SETshield do BCM

Define o estado de elevação necessária para um link de botão ou comando especificado para exibir um ícone com privilégios elevados. Envie essa mensagem explicitamente ou usando o [**botão \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Um **bool** que é **verdadeiro** para desenhar um ícone com privilégios elevados ou **false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 1 se for bem-sucedido ou um código de erro do contrário.

## <a name="remarks"></a>Comentários

Um aplicativo deve ser manifestado para usar comctl32.dll versão 6 para obter essa funcionalidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





