---
title: Autenticação com vários headers conhecidos
description: A estrutura HTTP MULTIPLE KNOWN HEADERS permite que os \_ \_ \_ aplicativos de servidor enviem vários desafios de autenticação para o cliente.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb8fd2071626d8a12f046ac0c3b6c50fcffc794462d5109a89a974f441879bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950925"
---
# <a name="authentication-with-multiple-known-headers"></a>Autenticação com vários headers conhecidos

A [**estrutura HTTP MULTIPLE KNOWN \_ \_ \_ HEADERS permite**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) que os aplicativos de servidor enviem vários desafios de autenticação para o cliente. Os aplicativos podem desafiá-lo com um único esquema de autenticação fornecendo o tipo de enumeração **HttpHeaderWwwAuthenticate** no membro **KnownHeaders** da estrutura [**CABEÇALHOS \_ \_**](/windows/desktop/api/Http/ns-http-http_response_headers) DE RESPOSTA HTTP contida em [**RESPOSTA HTTP. \_**](http-response.md) No entanto, quando o servidor enfrenta desafios com vários esquemas de autenticação, o aplicativo usa a estrutura [**HTTP \_ MULTIPLE KNOWN \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para fornecer os tipos de autenticação.

Quando o **sinalizador PRESERVE \_ \_ \_ \_ \_ ORDER DE** INFORMAÇÕES DE RESPOSTA HTTP estiver presente, HTTP enviará os cabeçalhos de autenticação na ordem especificada. Se o sinalizador não estiver presente, HTTP ordena os esquemas de autenticação do mais forte para o mais fraco da seguinte forma:

1.  Negotiate
2.  NTLM
3.  Digest
4.  Basic

Se o esquema de autenticação não for um desses esquemas, o aplicativo deverá especificar o **sinalizador PRESERVE \_ \_ \_ \_ \_ ORDER DE** SINALIZADORES DE INFORMAÇÕES DE RESPOSTA HTTP.

O **membro KnownHeader** de [**HTTP MULTIPLE KNOWN \_ \_ \_ HEADERS aponta**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para uma matriz de estruturas DE CABEÇALHO CONHECIDO [**\_ \_ HTTP.**](/windows/desktop/api/Http/ns-http-http_known_header) O **membro pRawValue** da estrutura **DE \_ \_ CABEÇALHO HTTP KNOWN** deve apontar para uma cadeia de caracteres que especifica o nome do esquema. HTTP analisará a cadeia de caracteres para determinar o esquema e executará uma das seguintes ações:

-   Se a cadeia de caracteres contiver um tipo de autenticação desconhecido ou se o tipo de autenticação não estiver habilitado no grupo de configuração (o grupo de URL ou a sessão do servidor) associado à solicitação, a API do Servidor HTTP anexará a cadeia de caracteres **em pRawValue** ao cabeçalho WWW-Authenticate. Por exemplo, se o aplicativo especificar um esquema de autenticação sem suporte e **pRawValue** contiver a cadeia de caracteres "CustomAuthString", o texto a seguir será anexado ao header de autenticação:

    WWW-Authenticate: CustomAuthSchemeCRLF

    Se o aplicativo não tiver a autenticação Básica habilitada e **pRawValue** contiver a cadeia de caracteres "Realm="BasicRealm"", o header de autenticação conterá o seguinte texto:

    WWW-Authenticate: Realm="BasicRealm"

-   Se a cadeia de caracteres contiver um tipo de autenticação conhecido e estiver presente no grupo de configuração (o grupo de URL ou a sessão do servidor) associado à solicitação, a API do Servidor HTTP gerará o cabeçalho WWW-Authenticate servidor. Por exemplo, se a cadeia de caracteres especificada em **pRawValue** for "Digest" e Digest estiver habilitada na sessão do servidor, a API do Servidor HTTP anexará o seguinte texto ao cabeçalho de autenticação:

    WWW-Authenticate: Digest realm=" testrealm@host.com "

Se o esquema no **membro pRawValue** do [**CABEÇALHO HTTP \_ KNOWN \_**](/windows/desktop/api/Http/ns-http-http_known_header) for Negotiate ou NTLM, o nome do esquema de autenticação será suficiente. Se o esquema especificado for Básico, o nome do realm será anexado ao nome do esquema; o aplicativo não precisa fornecer o nome do realm em **pRawValue.** Se o esquema especificado for Digest, HTTP [**chamará AcceptSecurityContext para**](../SecAuthN/acceptsecuritycontext--general.md) gerar o desafio que é anexado ao nome do esquema. Os parâmetros para o esquema Básico (realm) e Digest (realm e nome de domínio) são obtidos das informações de autenticação do grupo de configuração correspondentes.

Quando o aplicativo envia vários desafios de autenticação para o cliente em cabeçalhos de solicitação desconhecidos, a API do servidor HTTP os envia para o cliente sem intervenção. No entanto, esse uso não é recomendado.

 

 




