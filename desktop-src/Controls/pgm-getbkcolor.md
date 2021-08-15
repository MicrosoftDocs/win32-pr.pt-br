---
title: PGM_GETBKCOLOR mensagem (Commctrl.h)
description: Recupera a cor da tela de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetBkColor do Pager.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR controles Windows mensagem
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3ee3a4be09a948654d337a47eecdd2a7b15d16b0602016aa99500cd1c3728c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985936"
---
# <a name="pgm_getbkcolor-message"></a>Mensagem \_ GETBKCOLOR do PGM

Recupera a cor da tela de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ GetBkColor do Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor COLORREF** que contém a cor da tela de fundo atual.

## <a name="remarks"></a>Comentários

Por padrão, o controle pager usará a cor da face do botão do sistema como a cor da tela de fundo. Essa é a mesma cor que pode ser recuperada chamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) com COLOR \_ BTNFACE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

