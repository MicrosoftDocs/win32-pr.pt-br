---
title: ACK para Close-Session
description: Use o ACK para Close-Session pacote para confirmar a solicitação de Close-Session do cliente. O servidor envia a confirmação depois de liberar todos os recursos associados à sessão de carregamento.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- ACK para BITS de Close-Session
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289f2cfc2ca9f1e879e0aa592af28d86ae433f6e06d007aa71e00581baba2af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835409"
---
# <a name="ack-for-close-session"></a>ACK para Close-Session

Use a **confirmação do** pacote de sessão de fechamento para confirmar a solicitação de [**fechamento de sessão**](close-session.md) do cliente. O servidor envia a confirmação depois de liberar todos os recursos associados à sessão de carregamento.

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

GUID de cadeia de caracteres que identifica a sessão para o cliente. Substitua {GUID} pelo identificador de sessão que o cliente enviou no pacote de solicitação de [**fechamento de sessão**](close-session.md) . Se você não reconhece o identificador de sessão, defina o cabeçalho BITS-erro-código para a \_ sessão BG E \_ \_ não \_ encontrada.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo
</dt> <dd>

Substitua Length pelo número de bytes incluídos no corpo da resposta. O comprimento do conteúdo é necessário, mesmo que o corpo da resposta não inclua conteúdo.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erro-código
</dt> <dd>

Substitua o código de erro por um número hexadecimal que representa um valor HRESULT associado a um erro do lado do servidor. Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erro-contexto
</dt> <dd>

Substitua o contexto de erro por um número hexadecimal que represente o contexto no qual o erro ocorreu. Especifique o número hexadecimal para [**o \_ \_ \_ \_ arquivo remoto de contexto de erro BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se o servidor gerou o erro. Caso contrário, especifique o número hexadecimal para o **\_ \_ \_ \_ aplicativo remoto de contexto de erro BG** (0x7) se o erro foi gerado pelo aplicativo para o qual o arquivo de carregamento é passado. Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.

</dd> </dl>

## <a name="remarks"></a>Comentários

O cliente BITS reenviará o pacote de [**sessão de fechamento**](close-session.md) se o código de motivo estiver no intervalo de 500 a 599, a menos que o cabeçalho bits-erro-código esteja presente com um valor de sessão de BG \_ E \_ \_ não \_ encontrado. O cliente não tentará novamente os códigos de motivo 100 a 499.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ACK para cancelamento de sessão**](ack-for-cancel-session.md)
</dt> <dt>

[**Fechar sessão**](close-session.md)
</dt> </dl>

 

 




