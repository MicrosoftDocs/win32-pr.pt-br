---
title: Mensagem de WM_DDE_UNADVISE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de aviso de DDE do WM \_ \_ para informar a um aplicativo de servidor DDE que o item especificado ou um formato de área de transferência específico para o item não deve mais ser atualizado.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- Troca de dados de mensagem WM_DDE_UNADVISE
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455676"
---
# <a name="wm_dde_unadvise-message"></a>Mensagem de aviso de \_ DDE do WM \_

Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de **\_ \_ aviso de DDE do WM** para informar a um aplicativo de servidor DDE que o item especificado ou um formato de área de transferência específico para o item não deve mais ser atualizado. Isso encerra o link de dados quente ou ativo para o item especificado.

Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do cliente que está enviando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica o formato da área de transferência do item para o qual a solicitação de atualização está sendo cancelada. Se isso for **nulo**, todas as conversas de [**\_ \_ aviso DDE**](wm-dde-advise.md) ativos do WM para o item serão encerradas.

A palavra de ordem superior contém um átomo global que identifica o item para o qual a solicitação de atualização está sendo cancelada. Se isso for **nulo**, todos os links de [**\_ \_ aviso DDE**](wm-dde-advise.md) ativos do WM associados à conversa serão encerrados.

</dd> </dl>

## <a name="remarks"></a>Comentários

O aplicativo cliente aloca a palavra de ordem superior do *lParam* chamando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

O aplicativo de servidor posta a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positiva ou negativamente. Durante o lançamento do **\_ pacote de \_ ACK do WM DDE**, o servidor pode reutilizar o Atom ou pode excluir o Atom e criar um novo.

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

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK de DDE do WM \_**](wm-dde-ack.md)
</dt> <dt>

[**\_aviso de DDE do WM \_**](wm-dde-advise.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

