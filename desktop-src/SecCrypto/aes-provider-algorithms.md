---
description: A tabela a seguir lista os algoritmos com suporte do provedor criptográfico do Microsoft criptografia AES (AES).
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: Algoritmos do provedor AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5e197100060d53304bb5233560dcccae083756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755560"
---
# <a name="aes-provider-algorithms"></a>Algoritmos do provedor AES

A tabela a seguir lista os algoritmos com suporte do provedor criptográfico do Microsoft [*criptografia AES*](../secgloss/a-gly.md) (AES).



| ID do algoritmo       | Descrição                                                                                                                                                     | Comentários                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | DES triplo.                                                                                                                                                     | Comprimento da chave: 168 bits. Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum Salt permitido.<br/>                          |
| CALG \_ 3des \_ 112    | Criptografia [*Triple DES*](../secgloss/t-gly.md) de duas teclas.                                                            | Comprimento da chave: 112 bits. Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum Salt permitido.<br/>                          |
| CALG \_ AES \_ 128     | Algoritmo de criptografia de bloco AES.                                                                                                                                 | Comprimento da chave: 128 bits.                                                                                                                                      |
| CALG \_ AES \_ 192     | Algoritmo de criptografia de bloco AES.                                                                                                                                 | Comprimento da chave: 192 bits.                                                                                                                                      |
| CALG \_ AES \_ 256     | Algoritmo de criptografia de bloco AES.                                                                                                                                 | Comprimento da chave: 256 bits.                                                                                                                                      |
| CALG \_ des          | Criptografia DES.                                                                                                                                                 | Comprimento da chave: 56 bits. Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum Salt permitido.<br/>                           |
| \_HMAC CALG         | Algoritmo de hash com chave MAC.                                                                                                                                       | Computação HMAC.                                                                                                                                          |
| CALG \_ Mac          | Algoritmo de hash com chave de [*Message Authentication Code*](../secgloss/m-gly.md) (Mac). | Bloquear o MAC de codificação.                                                                                                                                          |
| CALG \_ MD2          | Algoritmo de hash MD2.                                                                                                                                          | Para obter mais informações, consulte [*algoritmo MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algoritmo de hash MD5.                                                                                                                                          | Para obter mais informações, consulte [*algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo de criptografia de bloco RC2.                                                                                                                                 | Comprimento da chave: 128 bits. Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Comprimento de Salt: pode ser definido.<br/>                  |
| CALG \_ RC4          | Algoritmo de criptografia de fluxo RC4.                                                                                                                                | Comprimento da chave: 128 bits. Comprimento de Salt: pode ser definido.<br/>                                                                                                  |
| CALG \_ RSA \_ KEYX    | Algoritmo de troca de chave pública RSA.                                                                                                                              | Comprimento da chave: pode ser definido, 384 bits a 16.384 bits em incrementos de 8 bits. Comprimento de chave padrão: 1.024 bits.<br/>                                            |
| CALG \_ \_ assinatura RSA    | Algoritmo de assinatura de chave pública RSA.                                                                                                                             | Comprimento da chave: pode ser definido, 384 bits a 16.384 bits em incrementos de 8 bits. Comprimento de chave padrão: 1.024 bits.<br/> A assinatura está em conformidade com o PKCS \# 6.<br/> |
| CALG \_ Sha          | Algoritmo de hash SHA.                                                                                                                                          | Para obter mais informações, consulte [*algoritmo de hash seguro*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | O mesmo que **CALG \_ Sha**.                                                                                                                                          | Para obter mais informações, consulte [*algoritmo de hash seguro*](../secgloss/s-gly.md).               |
| CALG \_ SHA \_ 256     | Algoritmo de hash SHA.                                                                                                                                          | Comprimento da chave: 256 bits. **Windows XP:** Não há suporte para esse algoritmo.<br/>                                                                           |
| CALG \_ SHA \_ 384     | Algoritmo de hash SHA.                                                                                                                                          | Comprimento da chave: 384 bits. **Windows XP:** Não há suporte para esse algoritmo.<br/>                                                                           |
| CALG \_ SHA \_ 512     | Algoritmo de hash SHA.                                                                                                                                          | Comprimento da chave: 512 bits. **Windows XP:** Não há suporte para esse algoritmo.<br/>                                                                           |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo de autenticação de cliente SSL3.                                                                                                                           | Para obter mais informações, consulte [Creating a CALG \_ SSL3 \_ SHAMD5 hash](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
