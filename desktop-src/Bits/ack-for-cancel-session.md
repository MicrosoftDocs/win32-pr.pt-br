---
title: ACK para Cancel-Session
description: Use o ACK para Cancel-Session pacote para confirmar a solicitação de Cancel-Session do cliente. O servidor envia a confirmação depois de liberar todos os recursos associados à sessão de carregamento.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- ACK para BITS de Cancel-Session
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85ff937b720a69ee2722cef2f02b25273ea58d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008572"
---
# <a name="ack-for-cancel-session"></a>ACK para Cancel-Session

Use o **ACK para o pacote Cancel-Session** para confirmar a solicitação de [**cancelamento da sessão**](cancel-session.md) do cliente. O servidor envia a confirmação depois de liberar todos os recursos associados à sessão de carregamento.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Cabeçalhos

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo
</dt> <dd>

Substitua o código de motivo pelo código de motivo HTTP. Por exemplo, defina código de motivo como 200 se êxito. Para obter uma lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-descrição
</dt> <dd>

Substitua Reason-Description pela descrição de HTTP associada ao código de motivo. Por exemplo, defina Reason-Description como OK se o código de motivo for 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote
</dt> <dd>

Identifica esse pacote de resposta como um pacote ACK.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão
</dt> <dd>

GUID de cadeia de caracteres que identifica a sessão para o cliente. Substitua {GUID} pelo identificador de sessão que o cliente enviou no pacote de solicitação de [**cancelamento de sessão**](cancel-session.md) . Se você não reconhece o identificador de sessão, defina o cabeçalho BITS-erro-código para a \_ sessão BG E \_ \_ não \_ encontrada.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo
</dt> <dd>

Substitua Length pelo número de bytes incluídos no corpo da resposta. Necessário mesmo se o corpo da resposta não incluir conteúdo.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erro-código
</dt> <dd>

Substitua o código de erro por um número hexadecimal que representa um valor HRESULT associado a um erro do lado do servidor. Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erro-contexto
</dt> <dd>

Substitua o contexto de erro por um número hexadecimal que represente o contexto no qual o erro ocorreu. Especifique o número hexadecimal para [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se o servidor tiver gerado o erro. Caso contrário, especifique o número hexadecimal para o **\_ \_ \_ \_ aplicativo remoto de contexto de erro BG** (0x7) se o erro foi gerado pelo aplicativo para o qual o arquivo de carregamento é passado. Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.

</dd> </dl>

## <a name="remarks"></a>Comentários

O cliente BITS reenviará o pacote de [**sessão cancelada**](cancel-session.md) se o código de motivo estiver no intervalo de 500 a 599, a menos que o cabeçalho bits-erro-código esteja presente com um valor de sessão de BG \_ E \_ \_ não \_ encontrado. O cliente não tentará novamente os códigos de motivo 100 a 499.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACK para fechamento de sessão**](ack-for-close-session.md)
</dt> <dt>

[**Cancelar sessão**](cancel-session.md)
</dt> </dl>

 

 




