---
title: Confirmação para fragmento
description: Use o ACK para o pacote de fragmento para reconhecer a solicitação de fragmento do cliente.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- ACK para BITS de fragmento
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103917770"
---
# <a name="ack-for-fragment"></a>Confirmação para fragmento

Use o **ACK para** o pacote de fragmento para reconhecer a solicitação de [**fragmento**](fragment.md) do cliente.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Cabeçalhos

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo
</dt> <dd>

Substitua o código de motivo por um código de motivo HTTP. A tabela a seguir mostra os códigos de motivo típicos para uma resposta a uma solicitação de [**fragmento**](fragment.md) . Para obter uma lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Código do motivo    | Descrição                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | OK. A solicitação foi bem-sucedida.<br/>                                                                             |
| 416<br/> | Intervalo-não satisfatório. O cliente enviou um fragmento cujo intervalo não é contíguo com o fragmento anterior.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-descrição
</dt> <dd>

Substitua Reason-Description pela descrição de HTTP associada ao código de motivo. Por exemplo, defina Reason-Description como OK se o código de motivo for 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote
</dt> <dd>

Identifica esse pacote de resposta como um pacote ACK.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-recebido-intervalo de conteúdo
</dt> <dd>

Deslocamento de base zero para o próximo byte que o servidor espera que o cliente envie. Por exemplo, se o fragmento contiver o intervalo de 128 212, você definiria intervalo como 213.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão
</dt> <dd>

GUID de cadeia de caracteres que identifica a sessão para o cliente. Substitua {GUID} pelo identificador de sessão que o cliente enviou no pacote de solicitação de [**fragmento**](fragment.md) . Se você não reconhece o identificador de sessão, defina o cabeçalho BITS-erro-código para a \_ sessão BG E \_ \_ não \_ encontrada.

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-responder-URL
</dt> <dd>

Contém a URL para os dados de resposta de um trabalho de upload-resposta. Inclua esse cabeçalho na resposta de fragmento final após a conclusão do upload e você receberá uma resposta do aplicativo de servidor, se aplicável.

Use o cabeçalho Content-Range da solicitação de fragmento para determinar se o carregamento foi concluído. O carregamento será concluído se o deslocamento final do valor do intervalo for igual ao valor de comprimento total menos um.

O servidor BITS posta o arquivo de upload no aplicativo de servidor depois de determinar que o carregamento foi concluído. O aplicativo de servidor processa o arquivo e gera a resposta. O servidor BITS define o valor de BITS-Reply-URL para a URL do arquivo de resposta do aplicativo de servidor.

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

Se a sessão for para um trabalho de resposta de upload, pode haver um atraso antes que o cliente receba a **confirmação final para** a resposta do fragmento. O comprimento do atraso depende da quantidade de tempo que o aplicativo de servidor (aplicativo no qual o servidor posta o arquivo de upload) leva para gerar a resposta.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Criar sessão**](create-session.md)
</dt> <dt>

[**Fragmento**](fragment.md)
</dt> </dl>

 

 





