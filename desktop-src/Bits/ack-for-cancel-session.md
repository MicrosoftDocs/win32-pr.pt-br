---
title: Ack para Cancel-Session
description: Use o Ack para Cancel-Session pacote para confirmar a solicitação de Cancel-Session cliente. O servidor envia a confirmação depois de liberar todos os recursos associados à sessão de upload.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Ack para Cancel-Session BITS
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23de0b23b0b87f559326c37ad61ecd09c38f697f0be48b45e92f5e7389b09fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588816"
---
# <a name="ack-for-cancel-session"></a>Ack para Cancel-Session

Use o **pacote Ack for Cancel-Session** para confirmar a solicitação [**Cancel-Session do**](cancel-session.md) cliente. O servidor envia a confirmação depois de liberar todos os recursos associados à sessão de upload.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>código-motivo
</dt> <dd>

Substitua o código de motivo pelo código de motivo HTTP. Por exemplo, de definir o código-motivo como 200 se for bem-sucedido. Para ver uma lista de códigos de motivo HTTP, [consulte RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Substitua reason-description pela descrição HTTP associada ao código do motivo. Por exemplo, de definido reason-description como OK se reason-code for 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Packet-Type
</dt> <dd>

Identifica esse pacote de resposta como um pacote Ack.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID de cadeia de caracteres que identifica a sessão para o cliente. Substitua {guid} pelo identificador de sessão que o cliente enviou no pacote de solicitação [**Cancelar Sessão.**](cancel-session.md) Se você não reconhecer o identificador de sessão, depure o header BITS-Error-Code como BG \_ E \_ SESSION NOT \_ \_ FOUND.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo
</dt> <dd>

Substitua length pelo número de bytes incluídos no corpo da resposta. Necessário mesmo se o corpo da resposta não incluir conteúdo.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

Substitua o código de erro por um número hexadecimal que representa um valor HRESULT associado a um erro do lado do servidor. Inclua esse header somente se reason-code não for 200 ou 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Bits-Error-Context
</dt> <dd>

Substitua o contexto de erro por um número hexadecimal que representa o contexto no qual o erro ocorreu. Especifique o número hexadecimal [**para BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se o servidor gerou o erro. Caso contrário, especifique o número hexadecimal para **BG \_ ERROR CONTEXT REMOTE \_ \_ \_ APPLICATION** (0x7) se o erro foi gerado pelo aplicativo para o qual o arquivo de upload é passado. Inclua esse header somente se o código-motivo não for 200 ou 201.

</dd> </dl>

## <a name="remarks"></a>Comentários

O cliente BITS resende o pacote [**Cancel-Session**](cancel-session.md) se o código-motivo estiver no intervalo de 500 a 599, a menos que o header BITS-Error-Code esteja presente com um valor de BG \_ E SESSION NOT \_ \_ \_ FOUND. O cliente não repetirá os códigos de motivo 100 a 499.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ack para close-session**](ack-for-close-session.md)
</dt> <dt>

[**Cancelar sessão**](cancel-session.md)
</dt> </dl>

 

 




