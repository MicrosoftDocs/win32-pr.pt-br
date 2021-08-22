---
description: O protocolo digest access
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: O protocolo digest access
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45fea65fc25df87ef434e7bfea5cb81690cdc06f82b72882438fe4475a1895b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916425"
---
# <a name="the-digest-access-protocol"></a>O protocolo digest access

O protocolo Digest Access especificado pelo [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) é implementado pelo SSP (provedor Microsoft Digest [*de suporte de*](../secgloss/s-gly.md) segurança) do Microsoft Digest. A implementação consiste em um conjunto de funções de contexto de segurança do SSPI [(Interface](sspi.md) do Provedor de Suporte de Segurança) da Microsoft que os aplicativos cliente/servidor chamam para:

-   Estabelecer um contexto [*de segurança para*](../secgloss/s-gly.md) troca de mensagens.
-   Obtenha objetos de dados exigidos pelo SSP digest, como [*credenciais e alças*](../secgloss/c-gly.md) de contexto.
-   Acessar mecanismos [*de confidencialidade*](../secgloss/i-gly.md) e integridade da mensagem.

A autenticação do Digest Access ocorre em transações de solicitação/resposta emparelhadas, com solicitações originadas no cliente e respostas originadas no servidor. Uma autenticação de Acesso Digest bem-sucedida requer dois pares de solicitação/resposta.

Quando o SSP digest é usado para autenticação HTTP, não há nenhuma conexão mantida entre o primeiro e o segundo par de solicitação/resposta. Em outras palavras, o servidor não aguarda a segunda solicitação depois de enviar a primeira resposta.

A ilustração a seguir mostra as etapas realizadas no caminho HTTP por um cliente e servidor para concluir uma autenticação usando o SSP digest. O mecanismo SASL usa a autenticação mútua, portanto, os dados de autenticação são enviados novamente na chamada final do servidor ASC para o cliente que verifica se o cliente está se comunicando com o servidor correto.

![protocolo de acesso digest](images/digest1.png)

O processo começa com o cliente solicitando um recurso protegido por acesso do servidor enviando a Solicitação HTTP 1.

O servidor recebe a Solicitação HTTP 1 e determina que o recurso requer informações de autenticação que não foram incluídas na solicitação. O servidor gera um desafio para o cliente da seguinte forma:

1.  O servidor obtém suas [*credenciais chamando*](../secgloss/c-gly.md) a [**função AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)
2.  O servidor gera o desafio Digest chamando a [**função AcceptSecurityContext (Geral).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
3.  O servidor envia um WWW-Authenticate como resposta à solicitação do cliente (mostrada como Resposta HTTP 1). O título contém o desafio Digest e uma diretiva opaca que contém uma referência a um contexto [*de*](../secgloss/s-gly.md) segurança parcial estabelecido para o cliente. O header é enviado com um código de status 401 que indica que a solicitação do cliente gerou um erro de acesso não autorizado. Para obter mais informações sobre o desafio digest, consulte [Conteúdo de um desafio digest e](contents-of-a-digest-challenge.md) [Gerando o desafio digest](generating-the-digest-challenge.md).
4.  O cliente recebe a Resposta HTTP 1, extrai o desafio Digest enviado pelo servidor e gera uma resposta de desafio Digest da seguinte forma:
    1.  As credenciais do usuário são obtidas chamando a função [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) ou solicitando interativamente as credenciais ao usuário.
    2.  As informações de desafio e credenciais são passadas para a [**função InitializeSecurityContext (Geral),**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) que gera a resposta de desafio digest.
5.  O cliente envia um cabeçalho de Autorização que contém a resposta de desafio para o servidor (mostrado como Solicitação HTTP 2). Para obter mais informações sobre [a](contents-of-a-digest-challenge-response.md) resposta de desafio digest, consulte Conteúdo de uma resposta de desafio digest e [Gerando](generating-the-digest-challenge-response.md)a resposta de desafio digest .
6.  O servidor recebe a Solicitação HTTP 2, extrai a resposta de desafio enviada pelo cliente e autentica as informações chamando a [**função AcceptSecurityContext (Geral).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Para obter detalhes sobre o processo de autenticação, consulte [Autenticação inicial usando Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  O servidor envia a Resposta HTTP 2 de volta para o cliente como a segunda e a resposta final exigidas pelo protocolo Digest Access. Se a autenticação for bem-sucedida, essa resposta conterá o recurso solicitado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conteúdo de uma resposta de desafio digest](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
