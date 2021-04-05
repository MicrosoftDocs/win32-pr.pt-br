---
description: As credenciais são exigidas pelo processo de autenticação Schannel; tanto o cliente quanto o servidor devem obter credenciais válidas para estabelecer um contexto de segurança para a troca de mensagens. Para obter um exemplo que demonstra esse procedimento, consulte obtendo credenciais.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Obtendo credenciais Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662134"
---
# <a name="obtaining-schannel-credentials"></a>Obtendo credenciais Schannel

As credenciais são exigidas pelo processo de autenticação Schannel; tanto o cliente quanto o servidor devem obter credenciais válidas para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) para a troca de mensagens. Para obter um exemplo que demonstra esse procedimento, consulte [obtendo credenciais](getting-a-certificate-for-schannel.md).

Seu aplicativo obtém credenciais chamando a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , que retorna um identificador para as credenciais solicitadas. Como os identificadores de credenciais são usados para armazenar informações de configuração, o mesmo identificador não pode ser usado para operações do lado do cliente e do servidor. Isso significa que os aplicativos que dão suporte a conexões de cliente e de servidor devem obter um mínimo de duas identificadores de credenciais.

No Windows XP, uma estrutura de [**\_ credenciais Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) especifica o seguinte:

-   Um protocolo de segurança
-   As codificações permitidas
-   Níveis mínimo e máximo de codificação
-   Um certificado [*X. 509*](../secgloss/x-gly.md) usado para autenticação — necessário para o servidor, opcional para o cliente, a menos que o servidor solicite a autenticação do cliente.

Passe a estrutura de [**\_ credenciais Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (por meio do parâmetro *pAuthData* ) para a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) . Essa função retorna o identificador de credenciais necessário para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md).

Para obter informações detalhadas sobre como definir as codificações usadas com Schannel, consulte [especificando codificações Schannel e níveis de codificação](specifying-schannel-ciphers-and-cipher-strengths.md).

Para obter informações sobre certificados, consulte [funções de repositório de certificados e](../seccrypto/cryptography-functions.md)certificados.

Para obter um exemplo que demonstra como abrir um [*repositório de certificados*](../secgloss/c-gly.md) e localizar um certificado a ser usado para autenticação Schannel, consulte [obter um certificado](getting-a-certificate-for-schannel.md).

 

 
