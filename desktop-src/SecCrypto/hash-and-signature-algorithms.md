---
description: Os seguintes algoritmos computam hashes e assinaturas digitais. Cada um desses algoritmos tem suporte nos provedores criptográficos de base, robustos e avançados da Microsoft.
ms.assetid: 91bf898d-658a-4e45-aa6e-eded46657563
title: Hash e algoritmos de assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1ca0819aebc01bba342410eda20b626349f1b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754601"
---
# <a name="hash-and-signature-algorithms"></a>Hash e algoritmos de assinatura

Os seguintes algoritmos computam [*hashes*](../secgloss/h-gly.md) e [*assinaturas digitais*](../secgloss/d-gly.md). Cada um desses algoritmos tem suporte nos provedores criptográficos de base, robustos e avançados da Microsoft. Os detalhes internos desses algoritmos estão além do escopo desta documentação. Para obter uma lista de fontes adicionais, consulte a [documentação adicional sobre criptografia](additional-documentation-on-cryptography.md).



| Algoritmos                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MAC CBC (encadeamento de blocos de codificação)<br/>     | Um dos algoritmos ( \_ Mac CALG) implementado pelos provedores da Microsoft é um Mac ( [*Message Authentication Code*](../secgloss/m-gly.md) de [*codificação de bloco*](../secgloss/b-gly.md) ). Esse método criptografa os dados base com uma codificação de bloco e, em seguida, usa o último bloco criptografado como o valor de [*hash*](../secgloss/h-gly.md) . O algoritmo de criptografia usado para criar o MAC é aquele que foi especificado quando a chave de sessão foi criada. <br/>                                                                            |
| HMAC<br/>                                | Um algoritmo ( \_ HMAC CALG) implementado por provedores da Microsoft. Esse algoritmo também usa uma [*chave simétrica*](../secgloss/s-gly.md) para criar o [*hash*](../secgloss/h-gly.md), mas é mais complexo do que o algoritmo de Mac CBC ( [*encadeamento de bloco de codificação*](../secgloss/c-gly.md) simples). Ele pode ser usado com qualquer algoritmo de hash criptográfico iterado, como MD5 ou SHA-1. Para obter detalhes, consulte [criando um HMAC](creating-an-hmac.md).<br/>                                                                                       |
| MD2, MD4 e MD5<br/>                   | Esses algoritmos de hash foram desenvolvidos pela RSA Data Security, Inc. Esses algoritmos foram desenvolvidos em ordem sequencial. Todos os três geram valores de hash de 128 bits. Todos os três são conhecidos por ter pontos fracos e devem ser usados apenas quando necessário para fins de compatibilidade. Para obter um novo código, recomendamos a família de hashes SHA-2.<br/> Esses algoritmos são bem conhecidos e podem ser revisados em detalhes em qualquer referência sobre [*criptografia*](../secgloss/c-gly.md).<br/>                                                                                                                                                           |
| Message Authentication Code (MAC)<br/>   | Os algoritmos MAC são semelhantes aos algoritmos de [*hash*](../secgloss/h-gly.md) , mas são computados usando uma chave [*simétrica*](../secgloss/s-gly.md) (sessão). A [*chave de sessão*](../secgloss/s-gly.md) original é necessária para recalcular o valor de hash. O valor de hash recalculado é usado para verificar se os dados base não foram alterados. Esses algoritmos, às vezes, são chamados de algoritmos com chave-hash. Para ver quais provedores da Microsoft oferecem suporte a MAC, consulte [provedores de serviços de criptografia da Microsoft](microsoft-cryptographic-service-providers.md).<br/>    |
| Algoritmo de hash seguro (SHA-1)<br/>       | Esse algoritmo de hash foi desenvolvido pelo [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) e pela NSA (National Security Agency). Esse algoritmo foi desenvolvido para uso com DSA (algoritmo de assinatura digital) ou DSS (padrão de assinatura digital). Esse algoritmo gera um valor de [*hash*](../secgloss/h-gly.md) de 160 bits. O SHA-1 é conhecido por ter pontos fracos e só deve ser usado quando necessário para fins de compatibilidade. Para obter um novo código, recomendamos a família de hashes SHA-2.<br/> |
| Algoritmo de hash seguro-2 (SHA-2)<br/>   | Esse algoritmo de hash foi desenvolvido como um sucessor para o SHA-1 pelo [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) e pela NSA (National Security Agency). Ele tem quatro variantes — SHA-224, SHA-256, SHA-384 e SHA-512 — que são nomeadas de acordo com o número de bits em suas saídas. Desses, SHA-256, SHA-384 e SHA-512 são implementados no provedor criptográfico do Microsoft AES.<br/>                                                                                                                                |
| Algoritmo de autorização de cliente SSL3<br/> | Esse algoritmo é usado para autenticação de cliente SSL3. No protocolo SSL3, uma concatenação de um hash MD5 e de um hash SHA é assinada com uma [*chave privada*](../secgloss/p-gly.md)RSA. CryptoAPI 2.0 e os provedores criptográficos aprimorados e base da Microsoft dão suporte a isso com o tipo de [*hash*](../secgloss/h-gly.md) CALG \_ SSL3 \_ SHAMD5. Para obter mais informações, consulte [Creating a CALG \_ SSL3 \_ SHAMD5 hash](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                                                                                                               |



 

 

 
