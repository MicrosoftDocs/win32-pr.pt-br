---
title: Mensagem de BCM_SETSHIELD (commctrl. h)
description: Define o estado de elevação necessária para um link de botão ou comando especificado para exibir um ícone com privilégios elevados. Envie essa mensagem explicitamente ou usando o botão \_ SetElevationRequiredState macro.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- Controles de BCM_SETSHIELD de mensagens do Windows
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
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085468"
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

## <a name="return-value"></a>Retornar valor

Retornará 1 se for bem-sucedido ou um código de erro do contrário.

## <a name="remarks"></a>Comentários

Um aplicativo deve ser manifestado para usar comctl32.dll versão 6 para obter essa funcionalidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





