---
description: O Provedor de Criptografia Base da Microsoft dá suporte aos algoritmos a seguir.
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: Algoritmos do provedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b6f3af49529ad46e70dd154c06febf433f5fb483861f7c0b2530af7ebbef2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879746"
---
# <a name="base-provider-algorithms"></a>Algoritmos do provedor base

O Provedor de Criptografia Base da Microsoft dá suporte aos algoritmos a seguir.



| ID do algoritmo                  | Descrição                                                                                                                                                               | Comentários                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ MD2<br/>          | Algoritmo de hash MD2<br/>                                                                                                                                          | Para obter mais informações, consulte [*Algoritmo MD2*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ MD5<br/>          | Algoritmo de hash MD5<br/>                                                                                                                                          | Para obter mais informações, consulte [*Algoritmo MD5*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ SHA<br/>          | Algoritmo de hash SHA<br/>                                                                                                                                          | Para obter mais informações, consulte [*Secure Hash Algorithm*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ SHA1<br/>         | O mesmo que CALG \_ SHA<br/>                                                                                                                                              | Para obter mais informações, consulte [*Secure Hash Algorithm*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ MAC<br/>          | [*Message Authentication Code*](../secgloss/m-gly.md) algoritmo de hash com chave (MAC)<br/> | Bloquear o MAC de criptografia.<br/>                                                                                                                                            |
| CALG \_ HMAC<br/>         | Algoritmo de hash com chave MAC<br/>                                                                                                                                       | Computação HMAC.<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHIMD5<br/> | Algoritmo de autenticação de cliente SLL3<br/>                                                                                                                           | Para obter mais informações, consulte [Criando um hash DE HASH DE \_ CALG SSL3 \_ SHIMD5](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                        |
| CALG \_ RSA \_ SIGN<br/>    | Algoritmo de assinatura de chave pública RSA<br/>                                                                                                                             | Comprimento da chave: pode ser definido de 384 bits a 16.384 bits em incrementos de 8 bits.<br/> Comprimento da chave padrão: 512 bits.<br/> A assinatura está em conformidade com o PKCS \# 6.<br/> |
| CALG \_ RSA \_ KEYX<br/>    | Algoritmo de troca de chaves públicas RSA<br/>                                                                                                                              | Comprimento da chave: pode ser definido de 384 bits a 1024 bits em incrementos de 8 bits.<br/> Comprimento da chave padrão: 512 bits.<br/>                                              |
| CALG \_ RC2<br/>          | Algoritmo de criptografia de bloco RC2<br/>                                                                                                                                 | Comprimento da chave: 40 bits.<br/> Modo padrão: encadeamento de blocos de criptografia.<br/> Tamanho do bloco: 64 bits.<br/> Comprimento do sal: 88 bits.<br/>                        |
| CALG \_ RC4<br/>          | Algoritmo de criptografia de fluxo RC4<br/>                                                                                                                                | Comprimento da chave: 40 bits.<br/> Comprimento do sal: 88 bits.<br/>                                                                                                        |
| CALG \_ DES<br/>          | Criptografia DES<br/>                                                                                                                                                 | Para obter mais informações, consulte [*DATA Encryption Standard*](../secgloss/d-gly.md) (DES).<br/>  |



 

 

 
