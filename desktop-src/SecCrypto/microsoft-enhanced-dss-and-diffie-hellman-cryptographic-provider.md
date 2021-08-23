---
description: O provedor criptográfico do Microsoft Enhanced DSS e Diffie-Hellman dá suporte a Diffie-Hellman troca de chaves, hash de SHA, assinatura de dados DSA e verificação (FIPS 186-2) e algoritmos de criptografia simétrica RC4.
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Provedor criptográfico do Microsoft Enhanced DSS & Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3eb3e70d90224b2d97612c5d63380171d3239e11915da4cdd8a38a0faea0b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425436"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Provedor criptográfico do Microsoft Enhanced DSS & Diffie-Hellman

O provedor criptográfico Enhanced DSS e [*Diffie-Hellman*](../secgloss/d-gly.md) da Microsoft dá suporte a troca *de chaves Diffie-Hellman* , hash SHA, assinatura de dados DSA e verificação (FIPS 186-2) e algoritmos de criptografia simétrica RC4.

<dl> Tipo de provedor: **Prov \_ DSS \_ DH**  
Nome do provedor: **ENH do MS- \_ \_ DSS \_ DH \_ Prov**  
</dl>

Este provedor criptográfico dá suporte aos seguintes algoritmos.

| ID do algoritmo          | Tipo de algoritmo  | Tamanho padrão (bits) | Descrição                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CALG \_ CYLINK \_ MEK** | Criptografia de dados | 40                  | Algoritmo de criptografia de mensagem CYLINK.                                                                                                                       |
| **CALG \_ RC2**         | Criptografia de dados | 128                 | RSA RC2.                                                                                                                                                   |
| **CALG \_ RC4**         | Criptografia de dados | 128                 | RSA RC4.                                                                                                                                                   |
| **CALG \_ des**         | Criptografia de dados | 56                  | DES (padrão de criptografia de dados).                                                                                                                            |
| **CALG \_ 3des \_ 112**   | Criptografia de dados | 112                 | Duas teclas DES triplas.                                                                                                                                        |
| **CALG \_ 3DES**        | Criptografia de dados | 168                 | Três teclas DES triplas.                                                                                                                                      |
| **CALG \_ SHA1**        | Hash            | 160                 | Secure Hash Algorithm 1 (SHA-1).                                                                                                                           |
| **CALG \_ MD5**         | Hash            | 128                 | Message Digest 5 (MD5).                                                                                                                                    |
| **\_sinal DSS \_ CALG**   | Assinatura       | 1024                | DSA (algoritmo de assinatura digital).                                                                                                                         |
| **CALG \_ DH \_ it**      | Troca de chaves    | 1024                | Armazene e encaminhe o algoritmo [*de troca de chaves Diffie-Hellman*](../secgloss/d-gly.md) . |
| **CALG \_ DH \_ EPHEM**   | Troca de chaves    | 1024                | Algoritmo efêmero [*Diffie-Hellman*](../secgloss/d-gly.md) .                      |



 

 

 
