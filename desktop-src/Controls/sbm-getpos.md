---
title: Mensagem de SBM_GETPOS (WinUser. h)
description: A \_ mensagem SBM GETPOS é enviada para recuperar a posição atual da caixa de rolagem de um controle de barra de rolagem.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- controles de Windows de mensagem de SBM_GETPOS
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0105b2c015614c9f064b2c97f60100c2240bd6588612d34b25546c7ced832bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408889"
---
# <a name="sbm_getpos-message"></a>\_Mensagem SBM GETPOS

A mensagem **SBM \_ GETPOS** é enviada para recuperar a posição atual da caixa de rolagem de um controle de barra de rolagem. A posição atual é um valor relativo que depende do intervalo de rolagem atual. Por exemplo, se o intervalo de rolagem for de 0 a 100 e a caixa de rolagem estiver no meio da barra, a posição atual será 50.

Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollPos** funcione corretamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é a posição atual da caixa de rolagem na barra de rolagem.

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

[**GetRange SBM \_**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**\_SETRANGE SBM**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

