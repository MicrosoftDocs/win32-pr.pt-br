---
title: Mensagem de WM_DDE_TERMINATE (DDE. h)
description: Um aplicativo troca dinâmica de dados (DDE) (cliente ou servidor) posta uma mensagem de encerramento de DDE do WM \_ \_ para encerrar uma conversa. Para postar essa mensagem, chame a função CreateMessage com os parâmetros a seguir.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- Troca de dados de mensagem WM_DDE_TERMINATE
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
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085430"
---
# <a name="wm_dde_terminate-message"></a>Mensagem de encerramento de \_ DDE do WM \_

Um aplicativo troca dinâmica de dados (DDE) (cliente ou servidor) posta uma mensagem de **\_ \_ encerramento de DDE do WM** para encerrar uma conversa.

Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela cliente ou servidor postando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="posting"></a>Lançamento

Ao aguardar a confirmação do encerramento, o aplicativo de lançamento não deve postar nenhuma outra mensagem para o aplicativo de recebimento. Se o aplicativo de envio receber mensagens (diferente do **WM \_ DDE \_ Terminate**) do aplicativo de recebimento, ele deverá excluir todos os átomos ou objetos de memória compartilhados que acompanham as mensagens, exceto os objetos de memória global associados às mensagens de [**\_ \_ dados DDE**](wm-dde-data.md) do [**WM \_ \_**](wm-dde-poke.md) ou do WM que não têm o conjunto de membros **fRelease** .

### <a name="receiving"></a>Recebimento

O aplicativo cliente ou servidor deve responder postando uma mensagem de **\_ \_ encerramento de DDE do WM** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>DDE. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_dados DDE do WM \_**](wm-dde-data.md)
</dt> <dt>

[**o WM \_ DDE. \_**](wm-dde-poke.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

