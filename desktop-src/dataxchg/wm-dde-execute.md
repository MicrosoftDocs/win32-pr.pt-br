---
title: Mensagem de WM_DDE_EXECUTE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de execução do WM \_ DDE \_ em um aplicativo de servidor DDE para enviar uma cadeia de caracteres ao servidor a ser processada como uma série de comandos.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- Troca de dados de mensagem WM_DDE_EXECUTE
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369679"
---
# <a name="wm_dde_execute-message"></a>Mensagem de execução de \_ DDE do WM \_

Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de **\_ \_ execução do WM DDE** em um aplicativo de servidor DDE para enviar uma cadeia de caracteres ao servidor a ser processada como uma série de comandos. Espera-se que o aplicativo de servidor poste uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) em resposta.

Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do cliente que está postando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Contém um objeto de memória global que faz referência a uma cadeia de caracteres de comando ANSI ou Unicode, dependendo dos tipos de janelas envolvidos na conversa.

</dd> </dl>

## <a name="remarks"></a>Comentários

A cadeia de caracteres de comando é uma cadeia de caracteres terminada em nulo que consiste em uma ou mais cadeias de código opcode entre colchetes simples ( \[ \] ). Cada cadeia de caracteres opcode tem a seguinte sintaxe, em que a lista de *parâmetros* é opcional:

*parâmetros de opcode*

O *opcode* é qualquer token único definido pelo aplicativo. Ele não pode incluir espaços, vírgulas, parênteses, colchetes ou aspas.

A lista de *parâmetros* pode conter qualquer valor ou valores definidos pelo aplicativo. Vários parâmetros são separados por vírgulas e a lista de parâmetros inteira é colocada entre parênteses. Os parâmetros não podem incluir vírgulas ou parênteses, exceto dentro de uma cadeia de caracteres entre aspas. Se um caractere de colchete ou parênteses for exibido em uma cadeia de caracteres entre aspas, ele não precisará ser duplicado, como foi o caso sob as regras antigas.

Veja a seguir as cadeias de caracteres de comando válidas:


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



Observe que, sob as regras antigas, os parênteses e colchetes tinham que ser duplicados, da seguinte maneira:


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



Os servidores devem ser capazes de analisar comandos em qualquer um dos formulários.

As cadeias de caracteres de execução Unicode devem ser usadas somente quando os identificadores de janela do cliente e do servidor fazem com que a função [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) retorne **true**.

### <a name="posting"></a>Lançamento

O aplicativo cliente aloca o objeto de memória global chamando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .

Ao processar a mensagem de [**\_ \_ confirmação de DDE do WM**](wm-dde-ack.md) que o servidor publica em resposta a uma mensagem de **\_ \_ execução de DDE do WM** , o aplicativo cliente deve excluir o objeto retornado pela mensagem de **\_ \_ confirmação DDE do WM** .

### <a name="receiving"></a>Recebimento

O aplicativo de servidor posta a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positiva ou negativamente. O servidor deve reutilizar o objeto de memória global.

A menos que especificado de outra forma por um subprotocolo, o servidor não deve postar a mensagem de [**\_ \_ ACK do WM DDE**](wm-dde-ack.md) até que todas as ações especificadas pela cadeia de caracteres de comando execute sejam concluídas. A única exceção a essa regra é quando a cadeia de caracteres faz com que o servidor encerre a conversa.

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

[**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
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

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

