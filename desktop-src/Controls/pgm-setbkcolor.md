---
title: Mensagem de PGM_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetBkColor do pager.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- controles de Windows de mensagem de PGM_SETBKCOLOR
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d727bf401fae3b8c58b96fe8b5190a3ad427abb40b0478d59de087add553ddf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830177"
---
# <a name="pgm_setbkcolor-message"></a>\_Mensagem SETBKCOLOR do PGM

Define a cor do plano de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBkColor do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor **COLORREF** que contém a nova cor de plano de fundo do controle de pager.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **COLORREF** que contém a cor do plano de fundo anterior.

## <a name="remarks"></a>Comentários

Por padrão, o controle de pager usará a cor de face do botão do sistema como a cor do plano de fundo. Essa é a mesma cor que pode ser recuperada chamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) com Color \_ btnface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

