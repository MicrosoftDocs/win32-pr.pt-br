---
title: Certificados SSL
description: O protocolo SSL (SSL) tornou-se um padrão para proteger as conexões de Internet e é usado para impedir a espionagem na rede. O protocolo SSL permite que um cliente e servidor autentiquem um ao outro e negociem algoritmos de criptografia.
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15e4e6f2b0fe9e3bb058ba506f8a36728540443
ms.sourcegitcommit: be2b23d847b9717224c5f31816594c8abda388a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "105758038"
---
# <a name="ssl-certificates"></a>Certificados SSL

O protocolo SSL (SSL), também conhecido como TLS, tornou-se um padrão para proteger as conexões de Internet e é usado para impedir a espionagem na rede. O protocolo SSL/TLS permite que um cliente e servidor autentiquem um ao outro e negociem algoritmos de criptografia.

O SSL usa uma chave de criptografia e um algoritmo de criptografia para proteger a conexão HTTP. As chaves de criptografia estão contidas em certificados SSL usados pelo cliente e pelo servidor. Normalmente, o certificado é um documento X. 509 ([RFC 2459](https://www.ietf.org/rfc/rfc2459.txt)). O servidor fornece o certificado SSL para a sessão e envia o certificado para o cliente na fase de handshake. O cliente enviará seu certificado ao servidor somente se o servidor enviar uma solicitação ao cliente para um certificado. Assim, o cliente sempre autentica o servidor, mas o servidor tem a opção de autenticar ou não o cliente.

Os certificados de servidor devem ser armazenados no armazenamento persistente local da API do servidor HTTP, para uso cada vez que uma conexão segura é criada. Cada entrada de repositório de certificados também contém o endereço IP e a porta do servidor, o hash de certificado (usado para assinar as mensagens) e a ID do aplicativo. A ID do aplicativo é usada para identificar o aplicativo que possui o certificado.

Os administradores do sistema podem armazenar informações de certificado do servidor SSL com as APIs de configuração. Uma ferramenta administrativa chama a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) e especifica o valor de HttpServiceConfigSSLCertInfo para o parâmetro de configuração de serviço para definir informações para um certificado SSL. Somente um certificado de servidor pode ser configurado para cada par de endereço IP e porta no computador. A API do servidor HTTP também fornece funções de [**consulta**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) e [**exclusão**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) para acessar ou excluir certificados existentes.

 

 




