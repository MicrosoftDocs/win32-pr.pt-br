---
description: Como o cliente, o servidor também adquire um identificador de credenciais para estar pronto para responder a uma solicitação de autenticação de entrada do cliente.
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: Inicialização do contexto do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1362c8fd71e079392f10a8e35f76ad511de3c49f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662127"
---
# <a name="server-context-initialization"></a>Inicialização do contexto do servidor

Como o cliente, o servidor também adquire um identificador de [*credenciais*](../secgloss/c-gly.md) para estar pronto para responder a uma solicitação de autenticação de entrada do cliente. As credenciais do servidor são usadas para autenticar o servidor no cliente em [*protocolos de segurança*](../secgloss/s-gly.md) que dão suporte à autenticação de servidor ou autenticação mútua. O servidor Obtém um identificador para suas credenciais definidas pela conta de serviço usada para iniciar o servidor. Ele faz isso chamando [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).

O servidor pode adquirir seu identificador de credenciais e entrar em um estado de escuta, ou pode aguardar um estado de escuta até que uma solicitação de conexão chegue e, em seguida, adquira um identificador de credenciais de entrada. Para obter mais informações sobre as funções de credenciais, consulte [Gerenciamento de credenciais](authentication-functions.md).

Quando o servidor recebe uma mensagem de solicitação de conexão de um cliente, ele cria um [*contexto de segurança*](../secgloss/s-gly.md) local para o cliente usando [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext). O servidor usa esse contexto de segurança local para realizar solicitações futuras pelo mesmo cliente. Para obter mais informações sobre funções de contexto, consulte [Gerenciamento de contexto](authentication-functions.md).

O servidor verifica o status de retorno e o descritor de buffer de saída para garantir que não haja erros até o momento, e pode rejeitar a solicitação de conexão se houver erros. Se houver informações no buffer de saída retornado por [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), ele agrupará esse buffer em uma mensagem de resposta para o cliente.

Qualquer buffer de saída de [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) deve ser enviado de volta ao cliente. Além disso, se o status de retorno exigir que o protocolo Continue (s \_ eu \_ continuar a \_ necessidade ou SEC \_ que \_ conclua \_ e \_ continuar), será necessária outra troca de mensagens com o cliente.

Para segmentos adicionais, o servidor aguarda que o cliente responda com outra mensagem. Essa espera pode ter atingido o tempo limite para evitar um ataque de negação de serviço em que um cliente nunca responde, causando um thread de servidor e, em breve, todos os threads de servidor, para parar de responder.

 

 
