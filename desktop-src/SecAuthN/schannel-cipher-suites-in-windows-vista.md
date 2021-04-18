---
description: Um conjunto de algoritmos de criptografia. Protocolos Schannel usam algoritmos de um pacote de criptografia para criar chaves e criptografar informações.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Pacotes de codificação do TLS no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cf270f0608666b7d766e3f063f24ea39204fd1
ms.sourcegitcommit: b022a50bc0d11975dad6337b8f399c47234dffcf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105752136"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Pacotes de codificação do TLS no Windows Vista

Um pacote de criptografia é um pacote de algoritmos criptográficos. Protocolos Schannel usam algoritmos de um pacote de criptografia para criar chaves e criptografar informações. Um pacote de criptografia especifica um algoritmo para cada uma das seguintes tarefas:

-   Troca de chaves
-   Criptografia em massa
-   Autenticação de mensagem

[*Algoritmos de troca de chaves*](../secgloss/k-gly.md) protegem as informações necessárias para criar chaves compartilhadas. Esses algoritmos são assimétricos ([*algoritmos de chave pública*](../secgloss/p-gly.md)) e têm um bom desempenho para quantidades relativamente pequenas de dados.

Algoritmos de criptografia em massa criptografam mensagens trocadas entre clientes e servidores. Esses algoritmos são [*simétricos*](../secgloss/s-gly.md) e têm um bom desempenho para grandes quantidades de dados.

Os algoritmos de [autenticação de mensagens](message-authentication-codes-in-schannel.md) geram [*hashes*](../secgloss/h-gly.md) de mensagens e assinaturas que garantem a [*integridade*](../secgloss/i-gly.md) de uma mensagem.

Os desenvolvedores especificam esses elementos usando tipos de dados de [**\_ ID de alg**](../seccrypto/alg-id.md) . Para obter mais informações, consulte [especificando codificações Schannel e níveis de codificação](specifying-schannel-ciphers-and-cipher-strengths.md).

O Schannel dá suporte aos seguintes conjuntos de codificação. Os pacotes são listados na ordem padrão em que são escolhidos pelo provedor Microsoft Schannel.

> [!IMPORTANT]
> Os serviços Web HTTP/2 falham com conjuntos de codificação não compatíveis com HTTP/2. Para garantir que seus serviços Web funcionem com clientes e navegadores HTTP/2, consulte [como implantar a ordenação personalizada do conjunto de codificação](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 



| Conjunto de codificação                                                 | Modo FIPS habilitado | Exchange              | Criptografia      | Hash            | Protocolos                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>                | Yes<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>                | Yes<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ com \_ RC4 \_ 128 \_ Sha<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>               | Yes<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/> | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P384<br/> | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/> | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/> | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P384<br/> | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/> | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>   | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P384<br/>   | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>   | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>   | Yes<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P384<br/>   | Yes<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ com \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>   | Yes<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 128 \_ CBC \_ Sha<br/>           | Yes<br/>    | FEITA<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ AES \_ 256 \_ CBC \_ Sha<br/>           | Yes<br/>    | FEITA<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ DHE \_ DSS \_ com \_ 3DES \_ ede \_ CBC \_ Sha<br/>          | Yes<br/>    | FEITA<br/>         | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ RC4 \_ 128 \_ MD5<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ com \_ MD5<br/>                      | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ com \_ MD5<br/>           | No<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| TLS \_ RSA \_ com \_ \_ MD5 nulo<br/>                         | No<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ com \_ \_ Sha nulo<br/>                         | No<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Os seguintes conjuntos de codificação têm suporte do Schannel; no entanto, eles não estão presentes por padrão. Eles devem ser adicionados conforme necessário. Para obter informações sobre como adicionar pacotes de codificação ao provedor Schannel, consulte [priorizando pacotes de codificação Schannel](prioritizing-schannel-cipher-suites.md).

-   \_Exportação RSA \_ TLS \_ com \_ RC4 \_ 40 \_ MD5
-   TLS \_ RSA \_ EXPORT1024 \_ com \_ RC4 \_ 56 \_ Sha
-   TLS \_ RSA \_ EXPORT1024 \_ com \_ des \_ CBC \_ Sha
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ des \_ 64 \_ CBC \_ com \_ MD5
-   TLS \_ RSA \_ com \_ des \_ CBC \_ Sha
-   TLS \_ RSA \_ com \_ \_ MD5 nulo
-   TLS \_ RSA \_ com \_ \_ Sha nulo
-   TLS \_ DHE \_ DSS \_ EXPORT1024 \_ com \_ des \_ CBC \_ Sha
-   TLS \_ DHE \_ DSS \_ com \_ des \_ CBC \_ Sha

**Windows Server 2003 e Windows XP:** Para obter informações sobre conjuntos de codificação com suporte, consulte os tópicos a seguir.

| Tópico                                                                         | Descrição                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Conjuntos de codificação TLS](tls-cipher-suites.md)<br/>                         | Informações sobre os conjuntos de codificação disponíveis com o protocolo TLS no Windows Server 2003 e no Windows XP.<br/>              |
| [Protocolo protocolo SSL](secure-sockets-layer-protocol.md)<br/> | Informações gerais sobre SSL 2,0 e 3,0, incluindo os pacotes de codificação disponíveis no Windows Server 2003 e no Windows XP.<br/> |



 

 

 
