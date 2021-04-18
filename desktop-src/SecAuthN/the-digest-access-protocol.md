---
description: O protocolo de acesso de resumo
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: O protocolo de acesso de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86aa8f05580c27c866c0568dbc67c4d5ba5c2016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556864"
---
# <a name="the-digest-access-protocol"></a>O protocolo de acesso de resumo

O protocolo de acesso de resumo especificado pela [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) é implementado pelo SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) da Microsoft Digest. A implementação consiste em um conjunto de funções de contexto de segurança SSPI ( [Microsoft Security Support Provider interface](sspi.md) ) que os aplicativos cliente/servidor chamam para:

-   Estabeleça um [*contexto de segurança*](../secgloss/s-gly.md) para a troca de mensagens.
-   Obter objetos de dados exigidos pelo SSP de resumo, como [*credenciais*](../secgloss/c-gly.md) e identificadores de contexto.
-   [*Integridade*](../secgloss/i-gly.md) de mensagens de acesso e mecanismos de confidencialidade.

A autenticação de acesso Digest ocorre em transações emparelhadas de solicitação/resposta, com solicitações originadas no cliente e respostas originadas no servidor. Uma autenticação de acesso de resumo bem-sucedida requer dois pares de solicitação/resposta.

Quando o SSP de resumo é usado para autenticação HTTP, não há nenhuma conexão mantida entre o primeiro e o segundo par de solicitação/resposta. Em outras palavras, o servidor não aguarda a segunda solicitação depois de enviar a primeira resposta.

A ilustração a seguir mostra as etapas executadas no caminho HTTP por um cliente e um servidor para concluir uma autenticação usando o SSP de resumo. O mecanismo SASL usa a autenticação mútua e, portanto, os dados de autenticação são enviados de volta à chamada do servidor ASC final para o cliente que verifica se o cliente está se comunicando com o servidor correto.

![Protocolo de acesso de resumo](images/digest1.png)

O processo começa com o cliente solicitando um recurso protegido por acesso do servidor enviando a solicitação HTTP 1.

O servidor recebe a solicitação HTTP 1 e determina que o recurso requer informações de autenticação que não foram incluídas na solicitação. O servidor gera um desafio para o cliente da seguinte maneira:

1.  O servidor obtém suas [*credenciais*](../secgloss/c-gly.md) chamando a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .
2.  O servidor gera o desafio de resumo chamando a função [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
3.  O servidor envia um cabeçalho de WWW-Authenticate como sua resposta à solicitação do cliente (mostrada como resposta HTTP 1). O cabeçalho contém o desafio de resumo e uma diretiva opaca que contém uma referência a um [*contexto de segurança*](../secgloss/s-gly.md) parcial estabelecido para o cliente. O cabeçalho é enviado com um código de status 401 que indica que a solicitação do cliente gerou um erro de acesso não autorizado. Para obter mais informações sobre o desafio de resumo, consulte [conteúdo de um desafio de resumo](contents-of-a-digest-challenge.md) e [gerando o desafio de resumo](generating-the-digest-challenge.md).
4.  O cliente recebe a resposta HTTP 1, extrai o desafio de resumo enviado pelo servidor e gera uma resposta de desafio de resumo da seguinte maneira:
    1.  As credenciais do usuário são obtidas chamando a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) ou, interativamente, solicitando credenciais ao usuário.
    2.  As informações de desafio e credenciais são passadas para a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) , que gera a resposta de desafio resumida.
5.  O cliente envia um cabeçalho de autorização que contém a resposta de desafio para o servidor (mostrado como solicitação HTTP 2). Para obter mais informações sobre a resposta de desafio de resumo, consulte [conteúdo de uma resposta de desafio de resumo](contents-of-a-digest-challenge-response.md) e [gerando a resposta de desafio Digest](generating-the-digest-challenge-response.md).
6.  O servidor recebe a solicitação HTTP 2, extrai a resposta de desafio enviada pelo cliente e autentica as informações chamando a função [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Para obter detalhes sobre o processo de autenticação, consulte [autenticação inicial usando Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  O servidor envia a resposta HTTP 2 de volta para o cliente como a segunda e última resposta exigida pelo protocolo de acesso Digest. Se a autenticação for bem-sucedida, essa resposta conterá o recurso solicitado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conteúdo de uma resposta de desafio de resumo](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
