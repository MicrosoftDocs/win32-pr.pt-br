---
description: Um pacote de criptografia é um pacote de algoritmos criptográficos.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Conjuntos de codificação em TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105748961"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>Conjuntos de codificação em TLS/SSL (Schannel SSP)

Um pacote de criptografia é um pacote de algoritmos criptográficos. A implementação do SSP do Schannel dos protocolos TLS/SSL usam algoritmos de um conjunto de codificação para criar chaves e criptografar informações. Um pacote de criptografia especifica um algoritmo para cada uma das seguintes tarefas:

-   Troca de chaves
-   Criptografia em massa
-   Autenticação de mensagem

[*Algoritmos de troca de chaves*](/windows/desktop/SecGloss/k-gly) protegem as informações necessárias para criar chaves compartilhadas. Esses algoritmos são assimétricos ([*algoritmos de chave pública*](/windows/desktop/SecGloss/p-gly)) e têm um bom desempenho para quantidades relativamente pequenas de dados.

Algoritmos de criptografia em massa criptografam mensagens trocadas entre clientes e servidores. Esses algoritmos são [*simétricos*](/windows/desktop/SecGloss/s-gly) e têm um bom desempenho para grandes quantidades de dados.

Os algoritmos de [autenticação de mensagens](message-authentication-codes-in-schannel.md) geram [*hashes*](/windows/desktop/SecGloss/h-gly) de mensagens e assinaturas que garantem a [*integridade*](/windows/desktop/SecGloss/i-gly) de uma mensagem.

Os desenvolvedores especificam esses elementos usando tipos de dados de [**\_ ID de alg**](/windows/desktop/SecCrypto/alg-id) . Para obter mais informações, consulte [especificando codificações Schannel e níveis de codificação](specifying-schannel-ciphers-and-cipher-strengths.md).

Nas versões anteriores do Windows, os conjuntos de criptografia TLS e as curvas elípticas foram configuradas usando uma única cadeia de caracteres:

![Diagrama que mostra uma única cadeia de caracteres para um conjunto de codificação.](images/tls-cipher-suite.png)

Versões diferentes do Windows dão suporte a diferentes conjuntos de criptografia TLS e ordem de prioridade. Consulte a versão correspondente do Windows para a ordem padrão na qual elas são escolhidas pelo provedor Microsoft Schannel.

**Windows Server 2022:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)

**Windows 10, versão 1903:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10, versão 1809:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10, versão 1803:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10, versão 1709:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10, versão 1703:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 e Windows 10, versão 1607:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10, versão 1511:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10, versão 1507:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 e Windows 8.1:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 8.1](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 e Windows 8:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 8](tls-cipher-suites-in-windows-8.md)

**Windows Server 2008 R2 e Windows 7:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows 7](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 e Windows Vista:** Para obter informações sobre conjuntos de codificação com suporte, consulte [pacotes de criptografia TLS no Windows Vista](schannel-cipher-suites-in-windows-vista.md)

**Windows Server 2003 e Windows XP:** Para obter informações sobre conjuntos de codificação com suporte, consulte os tópicos a seguir.

| Tópico                                                                         | Descrição                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Conjuntos de codificação TLS](tls-cipher-suites.md)<br/>                         | Informações sobre os conjuntos de codificação disponíveis com o protocolo TLS no Windows Server 2003 e no Windows XP.<br/>              |
| [Protocolo protocolo SSL](secure-sockets-layer-protocol.md)<br/> | Informações gerais sobre SSL 2,0 e 3,0, incluindo os pacotes de codificação disponíveis no Windows Server 2003 e no Windows XP.<br/> |



 

> [!Note]  
> Antes do Windows 10, as cadeias de caracteres do pacote de codificação foram anexadas com a curva elíptica para determinar a prioridade da curva. O Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica, portanto, o sufixo de curva elíptica não é necessário e é substituído pela nova ordem de prioridade de curva elíptica, quando fornecida, para permitir que as organizações usem a diretiva de grupo para configurar versões diferentes do Windows com os mesmos conjuntos de codificação.

 

