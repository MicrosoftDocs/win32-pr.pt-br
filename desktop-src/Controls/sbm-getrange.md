---
title: Mensagem de SBM_GETRANGE (WinUser. h)
description: A \_ mensagem GETrange do SBM é enviada para recuperar os valores mínimo e máximo da posição para o controle da barra de rolagem.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- Controles de SBM_GETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918861"
---
# <a name="sbm_getrange-message"></a>SBM \_ mensagem GETrange

A **mensagem \_ GetRange do SBM** é enviada para recuperar os valores mínimo e máximo da posição para o controle da barra de rolagem.

Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollRange** funcione corretamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para uma variável que recebe a posição de rolagem mínima.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma variável que recebe a posição de rolagem máxima.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**\_SETRANGE SBM**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

