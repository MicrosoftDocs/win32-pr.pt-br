---
description: Troca de cliente/servidor
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Troca de cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091326"
---
# <a name="clientserver-exchange"></a>Troca de cliente/servidor

Depois que um usuário tem um tíquete para um servidor, o cliente de estação de trabalho pode estabelecer uma sessão de comunicações segura com esse servidor.

**Para estabelecer uma sessão de comunicações segura com um servidor**

1.  O cliente envia ao servidor uma mensagem do tipo KRB \_ AP \_ req (solicitação de aplicativo Kerberos). Essa mensagem contém uma mensagem de autenticador que é criptografada com a chave enviada pelo [*centro de distribuição de chaves*](/windows/desktop/SecGloss/k-gly) (KDC) para a sessão com o servidor, o tíquete para sessões com o servidor e um sinalizador que indica se o cliente solicita autenticação mútua. Definir o sinalizador que solicita autenticação mútua é uma das opções na configuração do [*Kerberos*](/windows/desktop/SecGloss/k-gly). O usuário nunca será perguntado se a autenticação mútua deve ser usada.
2.  O servidor recebe o KRB \_ AP \_ req, descriptografa o tíquete e extrai os dados de autorização do usuário e a [*chave de sessão*](/windows/desktop/SecGloss/s-gly).
3.  O servidor usa a chave de sessão do tíquete para descriptografar a mensagem do autenticador do usuário e avalia o carimbo de data/hora dentro do.
4.  Se a mensagem do autenticador for válida, o servidor verificará o sinalizador de autenticação mútua na solicitação do cliente.
5.  Se o sinalizador de autenticação mútua estiver definido, o servidor usará a chave de sessão para criptografar a hora da mensagem do autenticador do usuário e retornará o resultado em uma mensagem do tipo KRB \_ AP \_ Rep (resposta do aplicativo Kerberos).
6.  Quando o cliente recebe o \_ Rep KRB AP \_ , ele descriptografa a mensagem de autenticador do servidor com a chave de sessão que ele compartilha com o servidor e compara o tempo enviado de volta pelo serviço com o tempo em sua mensagem de autenticador original. Se eles corresponderem, o cliente terá certeza de que o serviço é original e a conexão continuará.

 

 
