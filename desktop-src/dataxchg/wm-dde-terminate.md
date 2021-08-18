---
title: WM_DDE_TERMINATE mensagem (Dde.h)
description: Um Dados Dinâmicos Exchange (DDE) (cliente ou servidor) posta uma mensagem WM \_ DDE \_ TERMINATE para encerrar uma conversa. Para postar essa mensagem, chame a função PostMessage com os parâmetros a seguir.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE de dados de Exchange
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98d9b4bf2120cb6daa08b6088a8dd39f8a17b8e28c37a3917936a9c49230487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736263"
---
# <a name="wm_dde_terminate-message"></a>Mensagem WM \_ DDE \_ TERMINATE

Um Dados Dinâmicos Exchange (DDE) (cliente ou servidor) posta uma mensagem **WM \_ DDE \_ TERMINATE** para encerrar uma conversa.

Para postar essa mensagem, chame a [**função PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela do cliente ou do servidor que posta a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="posting"></a>Postar

Enquanto aguarda a confirmação do encerramento, o aplicativo de postagem não deve postar nenhuma outra mensagem para o aplicativo receptor. Se o aplicativo de envio receber mensagens (exceto **WM \_ DDE \_ TERMINATE**) do aplicativo receptor, ele deverá excluir os átomos ou objetos de memória compartilhada que acompanham as mensagens, exceto objetos de memória global associados a [**MENSAGENS WM \_ DDE WM DDE \_ OU**](wm-dde-poke.md) [**WM \_ DDE \_ DATA**](wm-dde-data.md) que não tenham o **membro fRelease** definido.

### <a name="receiving"></a>Recebimento

O aplicativo cliente ou servidor deve responder postando uma mensagem **WM \_ DDE \_ TERMINATE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Dde.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Sobre Dados Dinâmicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

