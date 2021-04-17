---
title: Mensagem de BM_SETDONTCLICK (WinUser. h)
description: Define um sinalizador em um botão de opção que controla a geração de \_ mensagens bilhão clicadas quando o botão recebe o foco.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- Controles de BM_SETDONTCLICK de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754382"
---
# <a name="bm_setdontclick-message"></a>\_Mensagem BM SETDONTCLICK

Define um sinalizador em um botão de opção que controla a geração de mensagens [bilhão \_ clicadas](bn-clicked.md) quando o botão recebe o foco.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um **bool** que especifica o estado. **True** para definir o sinalizador, caso contrário, **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado. Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

 





