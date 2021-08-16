---
description: A tabela a seguir lista os algoritmos com suporte pelo Provedor criptográfico do Microsoft criptografia AES (AES).
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: Algoritmos do provedor AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a06381c3f7fcf3d410a9a9a90c70633cab17c1ffd2e3e967ba6f3e7c3787fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773771"
---
# <a name="aes-provider-algorithms"></a>Algoritmos do provedor AES

A tabela a seguir lista os algoritmos com suporte pelo Provedor criptográfico do Microsoft [*criptografia AES*](../secgloss/a-gly.md) (AES).



| ID do algoritmo       | Descrição                                                                                                                                                     | Comentários                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | DES triplo.                                                                                                                                                     | Comprimento da chave: 168 bits. Modo padrão: encadeamento de blocos de criptografia.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum sal permitido.<br/>                          |
| CALG \_ 3DES \_ 112    | Criptografia [*DES triplo de duas*](../secgloss/t-gly.md) chaves.                                                            | Comprimento da chave: 112 bits. Modo padrão: encadeamento de blocos de criptografia.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum sal permitido.<br/>                          |
| CALG \_ AES \_ 128     | Algoritmo de criptografia de bloco AES.                                                                                                                                 | Comprimento da chave: 128 bits.                                                                                                                                      |
| CALG \_ AES \_ 192     | Algoritmo de criptografia de bloco AES.                                                                                                                                 | Comprimento da chave: 192 bits.                                                                                                                                      |
| CALG \_ AES \_ 256     | Algoritmo de criptografia de bloco AES.                                                                                                                                 | Comprimento da chave: 256 bits.                                                                                                                                      |
| CALG \_ DES          | Criptografia DES.                                                                                                                                                 | Comprimento da chave: 56 bits. Modo padrão: encadeamento de blocos de criptografia.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum sal permitido.<br/>                           |
| CALG \_ HMAC         | Algoritmo de hash com chave MAC.                                                                                                                                       | Computação HMAC.                                                                                                                                          |
| CALG \_ MAC          | [*Message Authentication Code*](../secgloss/m-gly.md) algoritmo de hash com chave (MAC). | Bloquear o MAC de criptografia.                                                                                                                                          |
| CALG \_ MD2          | Algoritmo de hash MD2.                                                                                                                                          | Para obter mais informações, consulte [*Algoritmo MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algoritmo de hash MD5.                                                                                                                                          | Para obter mais informações, consulte [*Algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo de criptografia de bloco RC2.                                                                                                                                 | Comprimento da chave: 128 bits. Modo padrão: encadeamento de blocos de criptografia.<br/> Tamanho do bloco: 64 bits.<br/> Comprimento do sal: pode ser definido.<br/>                  |
| CALG \_ RC4          | Algoritmo de criptografia de fluxo RC4.                                                                                                                                | Comprimento da chave: 128 bits. Comprimento do sal: pode ser definido.<br/>                                                                                                  |
| CALG \_ RSA \_ KEYX    | Algoritmo de troca de chaves públicas RSA.                                                                                                                              | Comprimento da chave: pode ser definido, 384 bits a 16.384 bits em incrementos de 8 bits. Comprimento da chave padrão: 1.024 bits.<br/>                                            |
| CALG \_ RSA \_ SIGN    | Algoritmo de assinatura de chave pública RSA.                                                                                                                             | Comprimento da chave: pode ser definido, 384 bits a 16.384 bits em incrementos de 8 bits. Comprimento da chave padrão: 1.024 bits.<br/> A assinatura está em conformidade com o PKCS \# 6.<br/> |
| CALG \_ SHA          | Algoritmo de hash SHA.                                                                                                                                          | Para obter mais informações, consulte [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | O mesmo que **CALG \_ SHA**.                                                                                                                                          | Para obter mais informações, consulte [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA \_ 256     | Algoritmo de hash SHA.                                                                                                                                          | Comprimento da chave: 256 bits. **Windows XP:** Não há suporte para esse algoritmo.<br/>                                                                           |
| CALG \_ SHA \_ 384     | Algoritmo de hash SHA.                                                                                                                                          | Comprimento da chave: 384 bits. **Windows XP:** Não há suporte para esse algoritmo.<br/>                                                                           |
| CALG \_ SHA \_ 512     | Algoritmo de hash SHA.                                                                                                                                          | Comprimento da chave: 512 bits. **Windows XP:** Não há suporte para esse algoritmo.<br/>                                                                           |
| CALG \_ SSL3 \_ SHIMD5 | Algoritmo de autenticação de cliente SSL3.                                                                                                                           | Para obter mais informações, consulte [Criando um hash DE HASH DE \_ CALG SSL3 \_ SHIMD5](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
