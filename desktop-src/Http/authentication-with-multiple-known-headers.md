---
title: Autenticação com vários cabeçalhos conhecidos
description: A \_ estrutura http \_ vários \_ cabeçalhos conhecidos permite que os aplicativos de servidor enviem vários desafios de autenticação para o cliente.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8afbce3c2a41ea143003723acebc7eb83dc463d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758812"
---
# <a name="authentication-with-multiple-known-headers"></a>Autenticação com vários cabeçalhos conhecidos

A [**estrutura \_ http \_ vários \_ cabeçalhos conhecidos**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) permite que os aplicativos de servidor enviem vários desafios de autenticação para o cliente. Os aplicativos podem desafiar o cliente com um único esquema de autenticação fornecendo o tipo de enumeração **HttpHeaderWwwAuthenticate** no membro **KnownHeaders** da estrutura [**de \_ \_ cabeçalhos de resposta http**](/windows/desktop/api/Http/ns-http-http_response_headers) contida [**na \_ resposta http**](http-response.md). No entanto, quando o servidor desafia com vários esquemas de autenticação, o aplicativo usa a estrutura [**http \_ vários \_ \_ cabeçalhos conhecidos**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) para fornecer os tipos de autenticação.

Quando os **\_ sinalizadores de informação de resposta http \_ \_ \_ preservam \_** o sinalizador de ordem, o http envia os cabeçalhos de autenticação na ordem especificada. Se o sinalizador não estiver presente, o HTTP ordenará os esquemas de autenticação do mais forte para o mais fraco da seguinte maneira:

1.  Negotiate
2.  NTLM
3.  Digest
4.  Básico

Se o esquema de autenticação não for um desses esquemas, o aplicativo deverá especificar o sinalizador de **\_ \_ \_ \_ \_ preservar sinalizadores de informações de resposta http** .

O membro **KnownHeader** de [**http \_ vários \_ \_ cabeçalhos conhecidos**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) aponta para uma matriz de estruturas de [**\_ \_ cabeçalho conhecidas http**](/windows/desktop/api/Http/ns-http-http_known_header) . O membro **pRawValue** da estrutura **de \_ \_ cabeçalho http conhecida** deve apontar para uma cadeia de caracteres que especifica o nome do esquema. O HTTP analisa a cadeia de caracteres para determinar o esquema e executa uma das seguintes ações:

-   Se a cadeia de caracteres contiver um tipo de autenticação desconhecido ou se o tipo de autenticação não estiver habilitado no grupo de configuração (o grupo de URLs ou a sessão de servidor) associada à solicitação, a API do servidor HTTP acrescentará a cadeia de caracteres em **pRawValue** ao cabeçalho WWW-Authenticate. Por exemplo, se o aplicativo especificar um esquema de autenticação sem suporte e **pRawValue** contiver a cadeia de caracteres "CustomAuthString", o texto a seguir será anexado ao cabeçalho de autenticação:

    WWW-Authenticate: CustomAuthSchemeCRLF

    Se o aplicativo não tiver a autenticação básica habilitada e **pRawValue** contiver a cadeia de caracteres "Basic realment =" BasicRealm "", o cabeçalho de autenticação conterá o seguinte texto:

    WWW-Authenticate: Realm básico = "BasicRealm"

-   Se a cadeia de caracteres contiver um tipo de autenticação conhecido e estiver presente no grupo de configuração (o grupo de URLs ou a sessão de servidor) associada à solicitação, a API do servidor HTTP gerará o cabeçalho WWW-Authenticate. Por exemplo, se a cadeia de caracteres especificada em **pRawValue** for "Digest" e o resumo estiver habilitado na sessão do servidor, a API do servidor http acrescentará o seguinte texto ao cabeçalho de autenticação:

    WWW-Authenticate: Digest Realm = " testrealm@host.com "

Se o esquema no membro **pRawValue** do [**cabeçalho http \_ conhecido \_**](/windows/desktop/api/Http/ns-http-http_known_header) for Negotiate ou NTLM, o nome do esquema de autenticação será suficiente. Se o esquema especificado for básico, o nome do Realm será anexado ao nome do esquema; o aplicativo não precisa fornecer o nome do realm em **pRawValue**. Se o esquema especificado for Digest, HTTP chamará [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) para gerar o desafio que é anexado ao nome do esquema. Os parâmetros de esquema básico (Realm) e Digest (Realm e nome de domínio) são obtidos das informações de autenticação do grupo de configuração correspondente.

Quando o aplicativo envia vários desafios de autenticação para o cliente em cabeçalhos de solicitação desconhecidos, a API do servidor HTTP envia-os para o cliente sem intervenção. No entanto, esse uso não é recomendado.

 

 




