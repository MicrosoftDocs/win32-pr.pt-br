---
title: Mensagem de PGM_GETBKCOLOR (commctrl. h)
description: Recupera a cor do plano de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetBkColor do pager.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- Controles de PGM_GETBKCOLOR de mensagens do Windows
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
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644906"
---
# <a name="pgm_getbkcolor-message"></a>\_Mensagem GETBKCOLOR do PGM

Recupera a cor do plano de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBkColor do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **COLORREF** que contém a cor do plano de fundo atual.

## <a name="remarks"></a>Comentários

Por padrão, o controle de pager usará a cor de face do botão do sistema como a cor do plano de fundo. Essa é a mesma cor que pode ser recuperada chamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) com Color \_ btnface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

