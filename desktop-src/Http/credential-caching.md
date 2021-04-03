---
title: Cache de credenciais
description: Cache de credenciais
ms.assetid: 6e411333-56fa-455b-a90a-f2b54f3c9545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a139d0cd90495de87f42de08687fd3157acaf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916461"
---
# <a name="credential-caching"></a>Cache de credenciais

## <a name="credential-caching-on-ntlm-ka-connections"></a>Cache de credenciais em conexões NTLM KA

A API do servidor HTTP armazena em cache as credenciais somente em conexões Keep-Alive (KA) para autenticação NTLM. Por padrão, a API do servidor HTTP armazena em cache as credenciais obtidas na primeira solicitação enviada em uma conexão KA. O cliente pode enviar solicitações subsequentes em conexões do KA sem um cabeçalho de autorização e obter a autenticação com base no contexto estabelecido anteriormente. Nesse caso, a API do servidor HTTP envia o token com base na credencial armazenada em cache para o aplicativo. As credenciais para uma solicitação enviada por um proxy não são armazenadas em cache. O aplicativo desabilita o cache de credenciais NTLM definindo o sinalizador **DisableNTLMCredentialCaching** na estrutura de [**\_ informações de \_ autenticação \_ do servidor http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) que é fornecida em chamadas para HttpSetServerSessionProperty ou HttpSetUrlGroupProperty. Quando o Caching de credenciais está desabilitado, a API do servidor HTTP descarta as credenciais armazenadas em cache e executa a autenticação para cada solicitação

## <a name="ntlm-credential-caching-for-specific-urls"></a>Cache de credenciais NTLM para URLs específicas

O aplicativo determina se as credenciais de solicitação retornadas pela API do servidor HTTP são armazenadas em cache inspecionando o parâmetro flags da \_ estrutura de informações de autenticação de solicitação HTTP \_ \_ . Esse parâmetro indica o \_ \_ \_ \_ token de sinalizador de autenticação de solicitação HTTP \_ para \_ credenciais em cache \_ quando o token NTLM retornado foi recuperado do cache. O cache de credenciais é especificado em um grupo de URLs para todas as URLs no grupo. Não há suporte para o Caching de credencial por URL, no entanto, os aplicativos podem determinar se aceitam ou rejeitam credenciais em cache por URL, verificando o \_ \_ token de \_ sinalizador de autenticação de solicitação HTTP \_ \_ para \_ o sinalizador de credenciais em cache \_ na estrutura de informações de autenticação de \_ solicitação HTTP \_ \_ . O aplicativo rejeita as credenciais armazenadas em cache enviando um desafio de autenticação 401 para o cliente. Em seguida, o cliente reenvia a solicitação com os cabeçalhos de autorização, disparando um novo handshake de autenticação com a API do servidor HTTP.

## <a name="basic-authentication"></a>Autenticação Básica

Quando um cabeçalho de autenticação básica é incluído na solicitação, a API do servidor HTTP analisa o cabeçalho para obter o nome de usuário e a senha. O nome de usuário é então analisado nas partes do usuário e do domínio. A API do servidor HTTP armazena em cache o token de acesso, obtido para a autenticação básica, com base no nome de usuário e na chave de domínio. Quando uma nova solicitação é recebida, a API do servidor HTTP recupera o token de acesso com base no nome de usuário e no domínio. A senha na solicitação é verificada em relação à senha armazenada em cache. O token de acesso em cache é excluído quando o limite de tempo de vida (TTL) é atingido.

 

 




