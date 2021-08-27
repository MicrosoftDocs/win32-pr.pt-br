---
description: As credenciais são exigidas pelo processo de autenticação Schannel; O cliente e o servidor devem obter credenciais válidas para estabelecer um contexto de segurança para troca de mensagens. Para obter um exemplo que demonstra esse procedimento, consulte Obter credenciais.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Obtendo credenciais Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216965d5b6fb1b21c36425242f54150112b2dcfb00dd7184c828aba865bbb5a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921194"
---
# <a name="obtaining-schannel-credentials"></a>Obtendo credenciais Schannel

As credenciais são exigidas pelo processo de autenticação Schannel; O cliente e o servidor devem obter credenciais válidas para estabelecer um contexto [*de segurança para*](../secgloss/s-gly.md) troca de mensagens. Para obter um exemplo que demonstra esse procedimento, consulte [Obter credenciais](getting-a-certificate-for-schannel.md).

Seu aplicativo obtém credenciais chamando a [**função AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) que retorna um identificador para as credenciais solicitadas. Como os alças de credenciais são usados para armazenar informações de configuração, o mesmo handle não pode ser usado para operações do lado do cliente e do servidor. Isso significa que os aplicativos que suportam conexões de cliente e de servidor devem obter um mínimo de dois alças de credenciais.

No Windows XP, uma [**estrutura \_ CRED SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) especifica o seguinte:

-   Um protocolo de segurança
-   As codificações que permitem
-   Pontos fortes mínimos e máximos de codificação
-   Um [*certificado X.509 usado para*](../secgloss/x-gly.md) autenticação – obrigatório para o servidor, opcional para o cliente, a menos que o servidor solicita a autenticação do cliente.

Passe a [**estrutura \_ CRED SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (por meio do parâmetro *pAuthData)* para [**a função AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Essa função retorna o handle de credenciais necessário para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md).

Para obter informações detalhadas sobre como definir as codificações usadas com o Schannel, consulte Especificando codificações [schannel e](specifying-schannel-ciphers-and-cipher-strengths.md)pontos fortes de criptografia.

Para obter informações sobre certificados, consulte Funções de certificado e [de armazenamento de certificados.](../seccrypto/cryptography-functions.md)

Para obter um exemplo [](../secgloss/c-gly.md) que demonstra como abrir um armazenamento de certificados e localizar um certificado a ser usado para autenticação Schannel, consulte [Getting a Certificate](getting-a-certificate-for-schannel.md).

 

 
