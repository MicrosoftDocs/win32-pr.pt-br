---
title: ACK para Create-Session
description: Use o ACK para Create-Session pacote para confirmar a solicitação de Create-Session do cliente.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- ACK para BITS de Create-Session
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "105748309"
---
# <a name="ack-for-create-session"></a>ACK para Create-Session

Use o **ACK para** o pacote de criação de sessão para confirmar a solicitação de [**criação de sessão**](create-session.md) do cliente.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Cabeçalhos

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo
</dt> <dd>

Substitua o código de motivo pelo código de motivo HTTP. A tabela a seguir mostra os códigos de motivo típicos para uma resposta a uma solicitação de [**criação de sessão**](create-session.md) . Para obter uma lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Código do motivo    | Descrição                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | OK. A solicitação foi bem-sucedida.<br/>                                          |
| 201<br/> | Criado. A sessão foi criada.<br/>                                        |
| 403<br/> | Negado. O usuário não tem permissão para carregar arquivos para a URL especificada.<br/> |
| 404<br/> | Não encontrado. A URL especificada não existe.<br/>                             |
| 409<br/> | Conflito. O arquivo existe no servidor e não pode ser substituído.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-descrição
</dt> <dd>

Substitua Reason-Description pela descrição de HTTP associada ao código de motivo. Por exemplo, defina Reason-Description como OK se o código de motivo for 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote
</dt> <dd>

Identifica esse pacote de resposta como um pacote ACK.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-protocolo
</dt> <dd>

GUID de cadeia de caracteres que identifica o protocolo que o servidor deseja usar para esta sessão. Substitua {GUID} pelo identificador de protocolo da lista de protocolos que o cliente inclui na solicitação de [**criação de sessão**](create-session.md) ; o cabeçalho BITS-supported-Protocol contém a lista. Inclua este cabeçalho somente se o código de motivo for 200 ou 201.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão
</dt> <dd>

GUID de cadeia de caracteres que identifica essa sessão para o cliente. Substitua {GUID} pelo identificador de sessão que o cliente envia em todos os pacotes de solicitação subsequentes.

O BITS usa um GUID para identificar a sessão, mas você pode usar qualquer cadeia de caracteres de HTTP-válido de até 100 caracteres.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-host-ID
</dt> <dd>

Opcional. Inclua este cabeçalho somente se a [propriedade de extensão do IIS do bits](bits-iis-extension-properties.md), BITSHostId, estiver definida. Substitua PublicHostName pelo nome do servidor ou endereço IP da propriedade BITSHostId.

O cliente deve substituir a parte do servidor da URL remota em todos os pacotes subsequentes. Se o cliente não especificar esse nome de host nos pacotes subsequentes, será possível que o trabalho comece novamente em outro servidor no farm, deixando um arquivo de carregamento parcial no servidor anterior.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-host-ID-fallback-tempo limite
</dt> <dd>

Opcional. Inclua este cabeçalho somente se o cabeçalho BITS-host-ID for especificado. Substitua o tempo limite pelo valor de tempo limite da propriedade BITSHostIdFallbackTimeout. A propriedade BITSHostIdFallbackTimeout é uma das [Propriedades de extensão do IIS do bits](bits-iis-extension-properties.md).

O cliente usa o período de tempo limite para determinar por quanto tempo ele tenta se reconectar ao nome do servidor especificado no cabeçalho BITS-host-ID antes de reverter para o nome de host especificado no nome de arquivo remoto do trabalho. O temporizador começa quando o BITS não consegue se conectar ao servidor BITS-host-ID. O temporizador é redefinido quando uma conexão com o servidor é restaurada. Se um período de tempo limite não for especificado, o cliente nunca será revertido para o nome de host especificado no nome do arquivo remoto.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Aceitação-codificação
</dt> <dd>

Identifica o esquema de codificação a ser usado nos fragmentos enviados ao servidor. O pacote de fragmento contém o fragmento codificado no corpo do pacote. O servidor BITS requer codificação de identidade (texto não criptografado). Inclua este cabeçalho somente se o código de motivo for 200 ou 201.

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

[**Criar sessão**](create-session.md)
</dt> </dl>

 

 





