---
description: Este tópico identifica as constantes que o WinHTTP usa.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f25ba011fdc97d55bae57c38a937a08177a6cefe2ecaaef3f85e2486e90956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114186"
---
# <a name="winhttp-constants"></a>Constantes do WinHTTP

O WinHTTP usa as seguintes constantes:

<dl>

<dt>

[**Mensagens de erro**](error-messages.md)
</dt> <dd>

Mensagens de erro específicas para as funções do WinHTTP. essas funções também retornam Windows mensagens de erro quando apropriado. O valor que corresponde a cada constante é o valor da constante para as funções da API (interface de programação de aplicativo) e os 16 bits inferiores do número do erro para o objeto [**WinHttpRequest**](winhttprequest.md) .

</dd> <dt>

[**Códigos de status HTTP**](http-status-codes.md)
</dt> <dd>

Constantes e valores correspondentes que indicam códigos de status HTTP retornados por servidores na Internet.

</dd> <dt>

[**Sinalizadores de opção**](option-flags.md)
</dt> <dd>

Sinalizadores de opção com suporte de [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Todos os sinalizadores de opção válidos têm um valor maior ou igual à \_ opção WinHTTP First \_ e menor ou igual à \_ última \_ opção WinHTTP.

</dd> <dt>

[**porta da INTERNET \_**](internet-port.md)
</dt> <dd>

Um valor de palavra que indica a porta.

</dd> <dt>

[**esquema de INTERNET \_**](internet-scheme.md)
</dt> <dd>

Esquemas de Internet com suporte do WinHTTP.

</dd>

<dt>

[**Sinalizadores de informações de consulta**](query-info-flags.md)
</dt>
<dd>

Atributos e modificadores usados por [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
</dd>

<dt>

**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**
</dt>
<dd>

Tem um valor de 0x00000001. Indica para [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) que as cadeias de caracteres passadas são cadeias de caracteres Unicode.
</dd>

<dt>

**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**
</dt>
<dd>

Tem um valor de 0x0000000000000001ull. Instrui o [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) a não concluir a chamada até que o buffer de dados fornecido tenha sido preenchido ou a resposta seja concluída. Passar esse sinalizador torna o comportamento de **WinHttpReadDataEx** equivalente ao de [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).
</dd>

</dl>
