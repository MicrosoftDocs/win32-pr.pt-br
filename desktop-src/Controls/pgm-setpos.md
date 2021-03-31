---
title: Mensagem de PGM_SETPOS (commctrl. h)
description: Define a posição de rolagem atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetPos do pager.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- Controles de PGM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644580"
---
# <a name="pgm_setpos-message"></a>\_Mensagem SETPOS do PGM

Define a posição de rolagem atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetPos do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor do tipo **int** que contém a nova posição de rolagem, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





