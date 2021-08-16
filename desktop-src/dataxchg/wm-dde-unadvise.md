---
title: WM_DDE_UNADVISE mensagem (Dde.h)
description: Um aplicativo cliente DDE (Dados Dinâmicos Exchange) posta uma mensagem WM \_ DDE UNADVISE para informar a um aplicativo de servidor DDE que o item especificado ou um formato de área de transferência específico para o item não deve mais \_ ser atualizado.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE dados de mensagem Exchange
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
ms.openlocfilehash: 9bbd0ac8e056cc43be764e745f824b50fc90b3cb2f0c50c9061d111fb3bc178d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915100"
---
# <a name="wm_dde_unadvise-message"></a>Mensagem WM \_ DDE \_ UNADVISE

Um aplicativo cliente DDE (Dados Dinâmicos Exchange) posta uma mensagem **WM \_ DDE \_ UNADVISE** para informar a um aplicativo de servidor DDE que o item especificado ou um formato de área de transferência específico para o item não deve mais ser atualizado. Isso encerra o link de dados quente ou quente para o item especificado.

Para postar essa mensagem, chame a [**função PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela do cliente que envia a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa especifica o formato da área de transferência do item para o qual a solicitação de atualização está sendo retirada. Se isso for **NULL,** todas [**as conversas ativas DO WM \_ DDE \_ ADVISE**](wm-dde-advise.md) para o item deverão ser encerradas.

A palavra de ordem alta contém um atom global que identifica o item para o qual a solicitação de atualização está sendo retirada. Se isso for **NULL,** todos os links [**ativos DO WM \_ DDE \_ ADVISE**](wm-dde-advise.md) associados à conversa deverão ser encerrados.

</dd> </dl>

## <a name="remarks"></a>Comentários

O aplicativo cliente aloca a palavra de ordem alta *de lParam* chamando a [**função GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

O aplicativo de servidor posta a [**mensagem WM \_ DDE \_ ACK**](wm-dde-ack.md) para responder positiva ou negativamente. Ao postar **o WM \_ DDE \_ ACK**, o servidor pode reutilizar o atom ou pode excluir o atom e criar um novo.

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

[**Globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
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

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Sobre Dados Dinâmicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

