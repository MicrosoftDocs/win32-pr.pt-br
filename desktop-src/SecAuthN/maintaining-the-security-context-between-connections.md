---
description: Para reduzir o tráfego do controlador de domínio e melhorar o desempenho, o lado do cliente do Microsoft Digest armazena em cache as informações recebidas após a autenticação bem-sucedida com um servidor.
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: Mantendo o contexto de segurança entre conexões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb450dde789f17f46397cb56fe74b94adcf8ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297078"
---
# <a name="maintaining-the-security-context-between-connections"></a>Mantendo o contexto de segurança entre conexões

Para reduzir o tráfego do controlador de domínio e melhorar o desempenho, o lado do cliente do Microsoft Digest armazena em cache as informações recebidas após a autenticação bem-sucedida com um servidor. Aplicativos cliente precisam apenas armazenar em cache o identificador para o [*contexto de segurança*](../secgloss/s-gly.md) que foi estabelecido. A tabela a seguir descreve as informações armazenadas em cache pelo pacote de segurança.



| Informações                                                       | Descrição                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome do servidor                                                       | O servidor que criou com êxito um contexto de segurança para o usuário.                                                                           |
| Realm/domínio                                                      | O nome de domínio usado na autenticação bem-sucedida.                                                                                              |
| [*Momentos*](../secgloss/n-gly.md) | Um nonce de servidor que está associado à autenticação bem-sucedida.                                                                               |
| Contagem de nonce                                                       | O número de vezes que o cliente incluiu o nonce em solicitações para o servidor. Isso é usado para detecção de repetição.                                 |
| Valor opaco                                                      | O valor retornado para a diretiva opaca após uma autenticação bem-sucedida. Esse valor contém uma referência ao contexto de segurança do usuário. |



 

Quando um cliente envia uma mensagem a um servidor, o servidor deve determinar se o cliente tem um contexto de segurança existente. Para fazer isso, o servidor passa cada solicitação de cliente para a função [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Essa função extrai o valor da diretiva opaca da solicitação, se presente, e a usa para pesquisar o contexto de segurança do cliente. Se o contexto de segurança for encontrado, o identificador do contexto será retornado ao servidor. Para obter informações relacionadas, consulte [Autenticando solicitações subsequentes](authenticating-subsequent-requests-using-microsoft-digest.md).

Como um meio de detectar ataques de falsificação e reprodução, o cliente chama a função [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) , que usa um contexto de segurança para assinar uma mensagem. Quando as mensagens são protegidas usando a função **MakeSignature** , o servidor usa a função [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) com o contexto em cache para verificar a origem e a [*integridade*](../secgloss/i-gly.md)da mensagem. Para obter mais informações, consulte [protegendo mensagens](protecting-messages-using-microsoft-digest.md).

 

 
