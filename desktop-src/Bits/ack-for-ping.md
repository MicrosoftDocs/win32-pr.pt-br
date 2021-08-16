---
title: ACK para ping
description: Use o ACK para o pacote de ping para confirmar a solicitação de ping do cliente.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- ACK para BITS de ping
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f31850599331027f3f8135a42dac8c8ea54519c04291d42fb06b5c7b8735fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835174"
---
# <a name="ack-for-ping"></a>ACK para ping

Use o **ACK para o pacote de ping** para confirmar a solicitação de [**ping**](ping.md) do cliente.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
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

Substitua o contexto de erro por um número hexadecimal que represente o contexto no qual o erro ocorreu. Especifique o número hexadecimal para [**o \_ \_ \_ \_ arquivo remoto de contexto de erro BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se o servidor gerou o erro. Caso contrário, especifique o número hexadecimal para o **\_ \_ \_ \_ aplicativo remoto de contexto de erro BG** (0x7) se o erro foi gerado pelo aplicativo para o qual o arquivo de carregamento é passado. Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 




