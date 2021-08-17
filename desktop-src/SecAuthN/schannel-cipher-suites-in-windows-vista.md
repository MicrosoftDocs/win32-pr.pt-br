---
description: Um conjunto de algoritmos criptográficos. Protocolos Schannel usam algoritmos de um pacote de criptografia para criar chaves e criptografar informações.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Pacotes de codificação do TLS no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf77d821612093e3015a0f8dee4cf51ae5bd9b95c653b61fe7a36271ba81ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918649"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Pacotes de codificação do TLS no Windows Vista

Um pacote de criptografia é um pacote de algoritmos criptográficos. Protocolos Schannel usam algoritmos de um pacote de criptografia para criar chaves e criptografar informações. Um pacote de criptografia especifica um algoritmo para cada uma das seguintes tarefas:

-   Troca de chaves
-   Criptografia em massa
-   Autenticação de mensagem

[*Algoritmos de troca de chaves*](../secgloss/k-gly.md) protegem as informações necessárias para criar chaves compartilhadas. Esses algoritmos são assimétricos ([*algoritmos de*](../secgloss/p-gly.md)chave pública) e têm um bom desempenho para quantidades relativamente pequenas de dados.

Algoritmos de criptografia em massa criptografam mensagens trocadas entre clientes e servidores. Esses algoritmos são [*simétricos e*](../secgloss/s-gly.md) têm um bom desempenho para grandes quantidades de dados.

[Algoritmos de](message-authentication-codes-in-schannel.md) autenticação de mensagem geram [*hashes*](../secgloss/h-gly.md) de mensagem e assinaturas que garantem a [*integridade*](../secgloss/i-gly.md) de uma mensagem.

Os desenvolvedores especificam esses elementos usando tipos [**de dados \_ de ID ALG.**](../seccrypto/alg-id.md) Para obter mais informações, consulte [Especificando codificações schannel e pontos fortes de codificação](specifying-schannel-ciphers-and-cipher-strengths.md).

O Schannel dá suporte aos seguintes pacote de criptografia. Os suites são listados na ordem padrão em que são escolhidos pelo Provedor Schannel da Microsoft.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com os suites de criptografia não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com navegadores e clientes HTTP/2, consulte [Como implantar a ordenação personalizada do conjunto de criptografias.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 



| Conjunto de criptografias                                                 | Modo FIPS habilitado | Exchange              | Criptografia      | Hash            | Protocolos                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>                | Yes<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>                | Yes<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ WITH \_ RC4 \_ 128 \_ SHA<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ 3DES \_ EDE \_ CBC \_ SHA<br/>               | Yes<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/> | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/> | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/> | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/> | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/> | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/> | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>   | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>   | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>   | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>   | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>   | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>   | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 128 \_ CBC \_ SHA<br/>           | Yes<br/>    | Dh<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ AES \_ 256 \_ CBC \_ SHA<br/>           | Yes<br/>    | Dh<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ WITH \_ 3DES \_ EDE \_ CBC \_ SHA<br/>          | Yes<br/>    | Dh<br/>         | 3DES<br/> | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ WITH \_ RC4 \_ 128 \_ MD5<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ WITH \_ MD5<br/>                      | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC \_ COM \_ MD5<br/>           | No<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| TLS \_ RSA \_ COM \_ \_ MD5 NULO<br/>                         | No<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA COM SHA \_ \_ \_ NULO<br/>                         | No<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Os seguintes pacote de criptografia têm suporte do Schannel; no entanto, eles não estão presentes por padrão. Eles devem ser adicionados conforme necessário. Para obter informações sobre como adicionar pacote de criptografia ao provedor Schannel, consulte [Priorizando os Schannel Cipher Suites.](prioritizing-schannel-cipher-suites.md)

-   EXPORTAÇÃO DE RSA TLS \_ \_ COM \_ \_ RC4 \_ 40 \_ MD5
-   TLS \_ RSA \_ EXPORT1024 \_ WITH \_ RC4 \_ 56 \_ SHA
-   TLS \_ RSA \_ EXPORT1024 \_ WITH \_ DES \_ CBC \_ SHA
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ DES \_ 64 \_ CBC \_ COM \_ MD5
-   TLS \_ RSA \_ WITH \_ DES \_ CBC \_ SHA
-   TLS \_ RSA \_ COM \_ \_ MD5 NULO
-   TLS \_ RSA COM SHA \_ \_ \_ NULO
-   TLS \_ DHE \_ DSS \_ EXPORT1024 \_ WITH \_ DES \_ CBC \_ SHA
-   TLS \_ DHE \_ DSS \_ WITH \_ DES \_ CBC \_ SHA

**Windows Server 2003 e Windows XP:** Para obter informações sobre os pacote de criptografia com suporte, consulte os tópicos a seguir.

| Tópico                                                                         | Descrição                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Conjunto de Criptografia TLS](tls-cipher-suites.md)<br/>                         | Informações sobre os suites de criptografia disponíveis com o protocolo TLS no Windows Server 2003 e Windows XP.<br/>              |
| [protocolo protocolo SSL](secure-sockets-layer-protocol.md)<br/> | Informações gerais sobre o SSL 2.0 e 3.0, incluindo os suites de criptografia disponíveis no Windows Server 2003 e Windows XP.<br/> |



 

 

 
