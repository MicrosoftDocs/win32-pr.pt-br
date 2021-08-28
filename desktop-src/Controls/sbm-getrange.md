---
title: Mensagem de SBM_GETRANGE (WinUser. h)
description: A \_ mensagem GETrange do SBM é enviada para recuperar os valores mínimo e máximo da posição para o controle da barra de rolagem.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- controles de Windows de mensagem de SBM_GETRANGE
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
ms.openlocfilehash: 8e66c6e7bf79c270d66fdeac0ece1a1ce82ed813d1638be3587be7237ecd30e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770036"
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

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



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

 

