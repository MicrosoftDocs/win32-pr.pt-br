---
description: O NTLM (desafio/resposta) do Windows é o protocolo de autenticação usado em redes que incluem sistemas que executam o sistema operacional Windows e sistemas autônomos.
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: NTLM da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9723f24d5913adefe70d4e238de0591790a34bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501592"
---
# <a name="microsoft-ntlm"></a>NTLM da Microsoft

O NTLM (desafio/resposta) do Windows é o protocolo de autenticação usado em redes que incluem sistemas que executam o sistema operacional Windows e sistemas autônomos.

O [*pacote de segurança*](../secgloss/s-gly.md) do Microsoft [*Kerberos*](../secgloss/k-gly.md) adiciona mais segurança do que o NTLM aos sistemas em uma rede. Embora o Microsoft *Kerberos* seja o protocolo de sua escolha, o NTLM ainda tem suporte. O NTLM também deve ser usado para autenticação de logon em sistemas autônomos. Para obter mais informações sobre o Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).

As credenciais NTLM são baseadas nos dados obtidos durante o processo de logon interativo e consistem em um nome de domínio, um nome de usuário e um [*hash*](../secgloss/h-gly.md) unidirecional da senha do usuário. O NTLM usa um protocolo criptografado de desafio/resposta para autenticar um usuário sem enviar a senha do usuário pela conexão. Em vez disso, o sistema que solicita autenticação deve executar um cálculo que prova que ele tem acesso às credenciais NTLM protegidas.

A autenticação interativa de NTLM em uma rede normalmente envolve dois sistemas: um sistema cliente, no qual o usuário está solicitando autenticação e um controlador de domínio, onde as informações relacionadas à senha do usuário são mantidas. A autenticação não interativa, que pode ser necessária para permitir que um usuário já conectado acesse um recurso como um aplicativo de servidor, normalmente envolve três sistemas: um cliente, um servidor e um controlador de domínio que faz os cálculos de autenticação em nome do servidor.

As etapas a seguir apresentam uma estrutura de autenticação não interativa de NTLM. A primeira etapa fornece as credenciais NTLM do usuário e ocorre somente como parte do processo de autenticação interativa (logon).

1.  (Somente autenticação interativa) Um usuário acessa um computador cliente e fornece um nome de domínio, nome de usuário e senha. O cliente computa um [*hash*](../secgloss/h-gly.md) criptográfico da senha e descarta a senha real.
2.  O cliente envia o nome de usuário para o servidor (em [*texto não criptografado*](../secgloss/p-gly.md)).
3.  O servidor gera um número aleatório de 16 bytes, chamado de *Challenge* ou [*nonce*](../secgloss/n-gly.md), e o envia para o cliente.
4.  O cliente criptografa esse desafio com o hash da senha do usuário e retorna o resultado para o servidor. Isso é chamado de *resposta*.
5.  O servidor envia os três itens a seguir para o controlador de domínio:

    -   Nome de usuário
    -   Desafio enviado ao cliente
    -   Resposta recebida do cliente

6.  O controlador de domínio usa o nome de usuário para recuperar o hash da senha do usuário do banco de dados do Gerenciador de contas de segurança. Ele usa esse hash de senha para criptografar o desafio.
7.  O controlador de domínio compara o desafio criptografado calculado (na etapa 6) com a resposta computada pelo cliente (na etapa 4). Se forem idênticos, a autenticação será bem-sucedida.

Seu aplicativo não deve acessar o [*pacote de segurança*](../secgloss/s-gly.md) NTLM diretamente; em vez disso, ele deve usar o pacote de segurança [*Negotiate*](../secgloss/n-gly.md) . Negociar permite que seu aplicativo aproveite os [*protocolos de segurança*](../secgloss/s-gly.md) mais avançados se eles tiverem suporte dos sistemas envolvidos na autenticação. Atualmente, o pacote de segurança Negotiate seleciona entre [*Kerberos*](../secgloss/k-gly.md) e NTLM. Negociar seleciona Kerberos, a menos que não possa ser usado por um dos sistemas envolvidos na autenticação.

 

 
