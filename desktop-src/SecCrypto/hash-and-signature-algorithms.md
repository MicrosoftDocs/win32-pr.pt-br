---
description: Os algoritmos a seguir computam hashes e assinaturas digitais. Cada um desses algoritmos tem suporte nos Provedores de Criptografia Base, Forte e Avançado da Microsoft.
ms.assetid: 91bf898d-658a-4e45-aa6e-eded46657563
title: Algoritmos de hash e assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c176b3a21ac5793f249f9aa7aceda897d53ea209f3e8e6bd260dc5ec529c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006604"
---
# <a name="hash-and-signature-algorithms"></a>Algoritmos de hash e assinatura

Os algoritmos a seguir computam [*hashes*](../secgloss/h-gly.md) e [*assinaturas digitais*](../secgloss/d-gly.md). Cada um desses algoritmos tem suporte nos Provedores de Criptografia Base, Forte e Avançado da Microsoft. Os detalhes internos desses algoritmos estão além do escopo desta documentação. Para obter uma lista de fontes adicionais, consulte [Documentação adicional sobre criptografia.](additional-documentation-on-cryptography.md)



| Algoritmos                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CBC (Encadeamento de Blocos de Criptografia) MAC<br/>     | Um dos algoritmos (CALG MAC) implementados pelos provedores da Microsoft é um \_ MAC (block [*cipher*](../secgloss/b-gly.md) [*Message Authentication Code).*](../secgloss/m-gly.md) Esse método criptografa os dados base com uma codificação de bloco e, em seguida, usa o último bloco criptografado como o [*valor de hash.*](../secgloss/h-gly.md) O algoritmo de criptografia usado para criar o MAC é aquele que foi especificado quando a chave de sessão foi criada. <br/>                                                                            |
| HMAC<br/>                                | Um algoritmo (CALG \_ HMAC) implementado pelos provedores da Microsoft. Esse algoritmo também usa uma [*chave simétrica*](../secgloss/s-gly.md) para criar o [*hash*](../secgloss/h-gly.md), mas é mais complexo do que o algoritmo MAC CBC (Cipher [*Block Chaining)*](../secgloss/c-gly.md) simples. Ele pode ser usado com qualquer algoritmo de hash criptográfico iterado, como MD5 ou SHA-1. Para obter detalhes, [consulte Criando um HMAC.](creating-an-hmac.md)<br/>                                                                                       |
| MD2, MD4 e MD5<br/>                   | Todos esses algoritmos de hash foram desenvolvidos pela RSA Data Security, Inc. Esses algoritmos foram desenvolvidos em ordem sequencial. Todos os três geram valores de hash de 128 bits. Todos os três são conhecidos por ter pontos fracos e só devem ser usados quando necessário para fins de compatibilidade. Para um novo código, recomendamos a família sha-2 de hashes.<br/> Esses algoritmos são bem conhecidos e podem ser revisados em detalhes em qualquer referência sobre [*criptografia.*](../secgloss/c-gly.md)<br/>                                                                                                                                                           |
| Message Authentication Code (MAC)<br/>   | Os algoritmos MAC são semelhantes aos algoritmos de [*hash,*](../secgloss/h-gly.md) mas são computados usando [*uma chave*](../secgloss/s-gly.md) simétrica (sessão). A chave [*de sessão original*](../secgloss/s-gly.md) é necessária para recomputar o valor de hash. O valor de hash recomputado é usado para verificar se os dados base não foram alterados. Às vezes, esses algoritmos são chamados de algoritmos de hash com chave. Para ver quais provedores da Microsoft são suportados pelo MAC, consulte [Microsoft Cryptographic Service Providers](microsoft-cryptographic-service-providers.md).<br/>    |
| Algoritmo de hash seguro (SHA-1)<br/>       | Esse algoritmo de hash foi desenvolvido pelo NIST (National [*Institute of Standards and Technology)*](../secgloss/n-gly.md) e pela NSA (National Security Agency). Esse algoritmo foi desenvolvido para uso com DSA (Algoritmo de Assinatura Digital) ou DSS (Assinatura Digital Standard). Esse algoritmo gera um valor de hash de 160 [*bits.*](../secgloss/h-gly.md) O SHA-1 é conhecido por ter pontos fracos e só deve ser usado quando necessário para fins de compatibilidade. Para um novo código, recomendamos a família sha-2 de hashes.<br/> |
| Algoritmo de hash seguro – 2 (SHA-2)<br/>   | Esse algoritmo de hash foi desenvolvido como um sucessor do SHA-1 pelo NIST (National [*Institute of Standards and Technology)*](../secgloss/n-gly.md) e pela NSA (National Security Agency). Ele tem quatro variantes — SHA-224, SHA-256, SHA-384 e SHA-512 — que são nomeadas de acordo com o número de bits em suas saídas. Desses, SHA-256, SHA-384 e SHA-512 são implementados no Provedor Criptográfico do Microsoft AES.<br/>                                                                                                                                |
| Algoritmo de autorização de cliente SSL3<br/> | Esse algoritmo é usado para autenticação de cliente SSL3. No protocolo SSL3, uma concatenação de um hash MD5 e um hash SHA é assinada com uma chave [*privada RSA*](../secgloss/p-gly.md). CryptoAPI 2.0 e os Provedores criptográficos de base e aprimorados da Microsoft são suportados com o tipo [*de hash*](../secgloss/h-gly.md) CALG \_ SSL3 \_ SHIMD5. Para obter mais informações, consulte [Criando um hash DE HASH DE \_ CALG SSL3 \_ SHIMD5](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                                                                                                               |



 

 

 
