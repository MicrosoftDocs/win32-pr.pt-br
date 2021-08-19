---
description: O provedor criptográfico aprimorado da Microsoft dá suporte aos seguintes algoritmos.
ms.assetid: d58bcd99-c54b-4fda-9fe1-e10a66707d81
title: Algoritmos de provedor aprimorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a8be464a57a482fa74fef07de097508508d7e965a5c20817ccbd884bb169e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766097"
---
# <a name="enhanced-provider-algorithms"></a>Algoritmos de provedor aprimorados

O [provedor criptográfico aprimorado da Microsoft](microsoft-enhanced-cryptographic-provider.md) dá suporte aos seguintes algoritmos.



| ID do algoritmo       | Descrição                                                                                                                                                     | Comentários                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | DES triplo.                                                                                                                                                     | Comprimento da chave: 168 bits. Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum Salt permitido.<br/>                           |
| CALG \_ 3des \_ 112    | Criptografia [*Triple DES*](../secgloss/t-gly.md) de duas teclas.                                                            | Comprimento da chave: 112 bits. Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum Salt permitido.<br/>                           |
| CALG \_ des          | Criptografia DES.                                                                                                                                                 | Comprimento da chave: 56 bits. Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Nenhum Salt permitido.<br/>                            |
| \_HMAC CALG         | Algoritmo de hash com chave MAC.                                                                                                                                       | Computação HMAC.                                                                                                                                          |
| CALG \_ Mac          | Algoritmo de hash com chave de [*Message Authentication Code*](../secgloss/m-gly.md) (Mac). | Bloquear o MAC de codificação.                                                                                                                                          |
| CALG \_ MD2          | Algoritmo de hash MD2.                                                                                                                                          | Para obter mais informações, consulte [*algoritmo MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algoritmo de hash MD5.                                                                                                                                          | Para obter mais informações, consulte [*algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo de criptografia de bloco RC2.                                                                                                                                 | Comprimento da chave: 128 bits. Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Comprimento de Salt: pode ser definido.<br/>                   |
| CALG \_ RC4          | Algoritmo de criptografia de fluxo RC4.                                                                                                                                | Comprimento da chave: 128 bits. Comprimento de Salt: pode ser definido.<br/>                                                                                                   |
| CALG \_ RSA \_ KEYX    | Algoritmo de troca de chave pública RSA.                                                                                                                              | Comprimento da chave: pode ser definido, 384 bits a 16.384 bits em incrementos de 8 bits. Comprimento de chave padrão: 1.024 bits.<br/>                                            |
| CALG \_ \_ assinatura RSA    | Algoritmo de assinatura de chave pública RSA.                                                                                                                             | Comprimento da chave: pode ser definido, 384 bits a 16.384 bits em incrementos de 8 bits. Comprimento de chave padrão: 1.024 bits.<br/> A assinatura está em conformidade com o PKCS \# 6.<br/> |
| CALG \_ Sha          | Algoritmo de hash SHA.                                                                                                                                          | Para obter mais informações, consulte [*algoritmo de hash seguro*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | O mesmo que CALG \_ Sha.                                                                                                                                              | Para obter mais informações, consulte [*algoritmo de hash seguro*](../secgloss/s-gly.md).               |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo de autenticação de cliente SSL3.                                                                                                                           | Para obter mais informações, consulte [Creating a CALG \_ SSL3 \_ SHAMD5 hash](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
