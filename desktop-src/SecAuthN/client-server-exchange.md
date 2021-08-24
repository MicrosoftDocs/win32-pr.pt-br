---
description: Cliente/servidor Exchange
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Cliente/servidor Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2401d3cf2bb59586e608bc7566c13009869d2874a1532b659f70c6c4e09e4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141169"
---
# <a name="clientserver-exchange"></a>Cliente/servidor Exchange

Depois que um usuário tem um tíquete para um servidor, o cliente da estação de trabalho pode estabelecer uma sessão de comunicação segura com esse servidor.

**Para estabelecer uma sessão de comunicação segura com um servidor**

1.  O cliente envia ao servidor uma mensagem do tipo KRB \_ AP \_ REQ (Solicitação de Aplicativo Kerberos). Essa mensagem contém uma mensagem de autenticador criptografada com a chave enviada pelo [*KDC (centro de distribuição de chaves)*](/windows/desktop/SecGloss/k-gly) para a sessão com o servidor, o tíquete para sessões com o servidor e um sinalizador que indica se o cliente solicita autenticação mútua. Definir o sinalizador que solicita autenticação mútua é uma das opções na configuração do [*Kerberos.*](/windows/desktop/SecGloss/k-gly) O usuário nunca é perguntado se a autenticação mútua deve ser usada.
2.  O servidor recebe o KRB \_ AP REQ, descriptografa o tíquete e extrai os dados de autorização do usuário e \_ a chave de [*sessão*](/windows/desktop/SecGloss/s-gly).
3.  O servidor usa a chave de sessão do tíquete para descriptografar a mensagem do autenticador do usuário e avalia o carimbo de data/hora dentro dele.
4.  Se a mensagem do autenticador for válida, o servidor verificará o sinalizador de autenticação mútua na solicitação do cliente.
5.  Se o sinalizador de autenticação mútua estiver definido, o servidor usará a chave de sessão para criptografar a hora da mensagem do autenticador do usuário e retornará o resultado em uma mensagem do tipo KRB AP REP (Resposta de Aplicativo \_ \_ Kerberos).
6.  Quando o cliente recebe o REP de AP do KRB, ele descriptografa a mensagem do autenticador do servidor com a chave de sessão que ele compartilha com o servidor e compara o tempo enviado de volta pelo serviço com o tempo em sua mensagem de \_ \_ autenticador original. Se eles corresponderem, o cliente tem certeza de que o serviço é original e que a conexão continua.

 

 
