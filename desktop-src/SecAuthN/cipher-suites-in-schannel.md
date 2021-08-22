---
description: Um pacote de criptografia é um pacote de algoritmos criptográficos.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Pacotes de Criptografia em TLS/SSL (SSP Schannel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590012b4a1ef0c84b8216fd970d1e60c8ed449294ec110dc566e7c3679b7bb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141210"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>Pacotes de Criptografia em TLS/SSL (SSP Schannel)

Um pacote de criptografia é um pacote de algoritmos criptográficos. A implementação SSP schannel dos protocolos TLS/SSL usa algoritmos de um pacote de criptografia para criar chaves e criptografar informações. Um pacote de criptografia especifica um algoritmo para cada uma das seguintes tarefas:

-   Troca de chaves
-   Criptografia em massa
-   Autenticação de mensagem

[*Algoritmos de troca de chaves*](/windows/desktop/SecGloss/k-gly) protegem as informações necessárias para criar chaves compartilhadas. Esses algoritmos são assimétricos ([*algoritmos de*](/windows/desktop/SecGloss/p-gly)chave pública) e têm um bom desempenho para quantidades relativamente pequenas de dados.

Algoritmos de criptografia em massa criptografam mensagens trocadas entre clientes e servidores. Esses algoritmos são [*simétricos e*](/windows/desktop/SecGloss/s-gly) têm um bom desempenho para grandes quantidades de dados.

[Algoritmos de](message-authentication-codes-in-schannel.md) autenticação de mensagem geram [*hashes*](/windows/desktop/SecGloss/h-gly) de mensagem e assinaturas que garantem a [*integridade*](/windows/desktop/SecGloss/i-gly) de uma mensagem.

Os desenvolvedores especificam esses elementos usando tipos [**de dados \_ de ID ALG.**](/windows/desktop/SecCrypto/alg-id) Para obter mais informações, consulte [Especificando codificações schannel e pontos fortes de codificação](specifying-schannel-ciphers-and-cipher-strengths.md).

Em versões anteriores do Windows, os suites de criptografia TLS e as curvas elípticas eram configurados usando uma única cadeia de caracteres:

![Diagrama que mostra uma única cadeia de caracteres para um Cipher Suite.](images/tls-cipher-suite.png)

Versões Windows diferentes são suportadas por diferentes conjunto de criptografias TLS e ordem de prioridade. Confira a versão Windows correspondente para a ordem padrão na qual elas são escolhidas pelo Provedor Schannel da Microsoft.

**Windows Server 2022:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)

**Windows 10, versão 1903:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10, versão 1809:** Para obter informações sobre os pacote de criptografia com suporte, consulte [TLS Cipher Suites no Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10, versão 1803:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10, versão 1709:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10, versão 1703:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 e Windows 10, versão 1607:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10, versão 1511:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10, versão 1507:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 e Windows 8.1:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 8.1](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 e Windows 8:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 8](tls-cipher-suites-in-windows-8.md)

**Windows Server 2008 R2 e Windows 7:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows 7](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 e Windows Vista:** Para obter informações sobre os suites de criptografia com suporte, consulte [TLS Cipher Suites no Windows Vista](schannel-cipher-suites-in-windows-vista.md)

**Windows Server 2003 e Windows XP:** Para obter informações sobre os pacote de criptografia com suporte, consulte os tópicos a seguir.

| Tópico                                                                         | Descrição                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Conjunto de Criptografia TLS](tls-cipher-suites.md)<br/>                         | Informações sobre os suites de criptografia disponíveis com o protocolo TLS no Windows Server 2003 e Windows XP.<br/>              |
| [protocolo SSL protocolo](secure-sockets-layer-protocol.md)<br/> | Informações gerais sobre o SSL 2.0 e 3.0, incluindo os suites de criptografia disponíveis no Windows Server 2003 e Windows XP.<br/> |



 

> [!Note]  
> Antes de Windows 10, as cadeias de caracteres do conjunto de criptografias eram anexadas com a curva elíptica para determinar a prioridade da curva. Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica para que o sufixo de curva elíptica não seja necessário e seja substituído pela nova ordem de prioridade de curva elíptica, quando fornecido, para permitir que as organizações usem a política de grupo para configurar versões diferentes do Windows com os mesmos grupos de criptografia.

 

