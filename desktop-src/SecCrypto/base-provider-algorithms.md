---
description: O provedor Microsoft Base Cryptographic oferece suporte aos seguintes algoritmos.
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: Algoritmos de provedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee99bc67769e0a7e91f2d0ecc635576336fd5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764624"
---
# <a name="base-provider-algorithms"></a>Algoritmos de provedor base

O provedor Microsoft Base Cryptographic oferece suporte aos seguintes algoritmos.



| ID do algoritmo                  | Descrição                                                                                                                                                               | Comentários                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ MD2<br/>          | Algoritmo de hash MD2<br/>                                                                                                                                          | Para obter mais informações, consulte [*algoritmo MD2*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ MD5<br/>          | Algoritmo de hash MD5<br/>                                                                                                                                          | Para obter mais informações, consulte [*algoritmo MD5*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ Sha<br/>          | Algoritmo de hash SHA<br/>                                                                                                                                          | Para obter mais informações, consulte [*algoritmo de hash seguro*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ SHA1<br/>         | Igual ao CALG \_ Sha<br/>                                                                                                                                              | Para obter mais informações, consulte [*algoritmo de hash seguro*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ Mac<br/>          | Algoritmo de hash com chave de [*Message Authentication Code*](../secgloss/m-gly.md) (Mac)<br/> | Bloquear o MAC de codificação.<br/>                                                                                                                                            |
| \_HMAC CALG<br/>         | Algoritmo de hash com chave de MAC<br/>                                                                                                                                       | Computação HMAC.<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHAMD5<br/> | Algoritmo de autenticação de cliente SLL3<br/>                                                                                                                           | Para obter mais informações, consulte [Creating a CALG \_ SSL3 \_ SHAMD5 hash](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                        |
| CALG \_ \_ assinatura RSA<br/>    | Algoritmo de assinatura de chave pública RSA<br/>                                                                                                                             | Comprimento da chave: pode ser definido de 384 bits a 16.384 bits em incrementos de 8 bits.<br/> Comprimento de chave padrão: 512 bits.<br/> A assinatura está em conformidade com o PKCS \# 6.<br/> |
| CALG \_ RSA \_ KEYX<br/>    | Algoritmo de troca de chave pública RSA<br/>                                                                                                                              | Comprimento da chave: pode ser definido de 384 bits a 1024 bits em incrementos de 8 bits.<br/> Comprimento de chave padrão: 512 bits.<br/>                                              |
| CALG \_ RC2<br/>          | Algoritmo de criptografia de bloco RC2<br/>                                                                                                                                 | Comprimento da chave: 40 bits.<br/> Modo padrão: encadeamento de blocos de codificação.<br/> Tamanho do bloco: 64 bits.<br/> Comprimento de Salt: 88 bits.<br/>                        |
| CALG \_ RC4<br/>          | Algoritmo de criptografia de fluxo RC4<br/>                                                                                                                                | Comprimento da chave: 40 bits.<br/> Comprimento de Salt: 88 bits.<br/>                                                                                                        |
| CALG \_ des<br/>          | Criptografia DES<br/>                                                                                                                                                 | Para obter mais informações, consulte [*padrão de criptografia de dados*](../secgloss/d-gly.md) (des).<br/>  |



 

 

 
