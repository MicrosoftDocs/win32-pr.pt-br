---
description: Os provedores associados à CryptoAPI (API de criptografia) são chamados de CSPs (provedores de serviços de criptografia) nesta documentação.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Provedores de serviço de criptografia CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b3820a0d45534bc5c492d843352be038f7ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090741"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Provedores de serviço de criptografia CryptoAPI

Os provedores associados à [*CryptoAPI*](/windows/desktop/SecGloss/c-gly)(API de criptografia) são chamados de CSPs (provedores de serviços de criptografia) nesta documentação. Normalmente, os CSPs implementam algoritmos criptográficos e fornecem armazenamento de chaves. Os provedores associados à CNG, por outro lado, separam a implementação de algoritmos do armazenamento de chaves. Os seguintes CSPs da Microsoft são distribuídos com o Windows Vista e o Windows Server 2008.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Microsoft Base Cryptographic Provider v1.0

Implementa os seguintes algoritmos para fazer hash, assinar e criptografar conteúdo.



| Nome                                            | Uso          | Tipo  | Tamanho da chave (padrão/min/máx.) |
|-------------------------------------------------|--------------|-------|----------------------------|
| DES (padrão de criptografia de dados)                  | Criptografia   | Bloquear | 56/56/56                   |
| Soma de verificação de autenticação de mensagem com hash (HMAC)   | Hash      | Qualquer   | 0/0/0                      |
| Soma de verificação de autenticação de mensagem (MAC)           | Hash      | Qualquer   | 0/0/0                      |
| Mensagem Digest 2 (MD2)                          | Hash      | Qualquer   | 128/128/128                |
| Mensagem Digest 4 (MD4)                          | Hash      | Qualquer   | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear | 40/40/56                   |
| RC4 (RSA Data Security 4)                       | Criptografia   | Bloquear | 40/40/56                   |
| Troca de chaves RSA                                | Troca de chaves | RSA   | 512/384/1024               |
| Assinatura RSA                                   | Assinando      | RSA   | 512/384/16384              |
| Algoritmo de hash seguro (SHA1)                    | Hash      | Qualquer   | 160/160/160                |
| Secure Socket Layer 3 SHA and MD5 (SSL3 SHAMD5) | Hash      | Qualquer   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Base DSS e Diffie-Hellman provedor criptográfico

Implementa os seguintes algoritmos para dar suporte a hashing, assinatura, criptografia e Diffie-Hellman troca de chaves.



| Nome                                  | Uso          | Tipo           | Tamanho da chave (padrão/min/máx.) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo de criptografia de mensagem CYLINK   | Criptografia   | Bloquear          | 40/40/40                   |
| DES (padrão de criptografia de dados)        | Criptografia   | Bloquear          | 56/56/56                   |
| Algoritmo de troca de chave Diffie-Hellman | Troca de chaves | Diffie-Hellman | 512/512/1024               |
| Diffie-Hellman algoritmo efêmero    | Troca de chaves | Diffie-Hellman | 512/512/1024               |
| Algoritmo de assinatura digital (DSA)     | Assinando      | DSS            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hash      | Qualquer            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Criptografia   | Bloquear          | 40/40/56                   |
| RC4 (RSA Data Security 4)             | Criptografia   | Stream         | 40/40/56                   |
| Algoritmo de hash seguro (SHA1)          | Hash      | Qualquer            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Microsoft Base DSS Cryptographic Provider

Implementa os seguintes algoritmos para assinar e fazer hash de conteúdo:



| Nome                              | Uso     | Tipo | Tamanho da chave (padrão/min/máx.) |
|-----------------------------------|---------|------|----------------------------|
| Algoritmo de assinatura digital (DSA) | Assinando | DSS  | 1024/512/1024              |
| Message Digest 5 (MD5)            | Hash | Qualquer  | 128/128/128                |
| Algoritmo de hash seguro (SHA1)      | Hash | Qualquer  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Microsoft Base Smart Card Crypto Provider

O oferece suporte a cartões inteligentes e implementa os seguintes algoritmos para fazer hash, assinar e criptografar conteúdo.

| Nome                                            | Uso          | Tipo   | Tamanho da chave (padrão/min/máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Criptografia AES 128 (AES128)       | Criptografia   | Bloquear  | 128/128/128                |
| Criptografia AES 192 (AES192)       | Criptografia   | Bloquear  | 192/192/192                |
| Criptografia AES 256 (AES256)       | Criptografia   | Bloquear  | 256/256/256                |
| DES (padrão de criptografia de dados)                  | Criptografia   | Bloquear  | 56/56/56                   |
| Dois DES triplos principais                              | Criptografia   | Bloquear  | 112/112/112                |
| Três teclas DES triplas                            | Criptografia   | Bloquear  | 168/168/168                |
| Soma de verificação de autenticação de mensagem com hash (HMAC)   | Hash      | Qualquer    | 0/0/0                      |
| Soma de verificação de autenticação de mensagem (MAC)           | Hash      | Qualquer    | 0/0/0                      |
| Mensagem Digest 2 (MD2)                          | Hash      | Qualquer    | 128/128/128                |
| Mensagem Digest 4 (MD4)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear  | 128/40/128                 |
| RC4 (RSA Data Security 4)                       | Criptografia   | Stream | 128/40/128                 |
| Troca de chaves RSA                                | Troca de chaves | RSA    | 1024/1024/4096             |
| Assinatura RSA                                   | Assinando      | RSA    | 1024/1024/4096             |
| Algoritmo de hash seguro (SHA1)                    | Hash      | Qualquer    | 160/160/160                |
| Algoritmo de hash seguro 256 (SHA256)              | Hash      | Qualquer    | 256/256/256                |
| Algoritmo de hash seguro 384 (SHA384)              | Hash      | Qualquer    | 384/384/384                |
| Algoritmo de hash seguro 512 (SHA512)              | Hash      | Qualquer    | 512/512/512                |
| Secure Socket Layer 3 SHA and MD5 (SSL3 SHAMD5) | Hash      | Qualquer    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Provedor criptográfico Schannel do Microsoft DH

Dá suporte ao pacote de segurança Schannel (canal seguro) que implementa os protocolos de autenticação protocolo SSL (SSL) e TLS (Transport Layer Security). Esse CSP também dá suporte à Diffie-Hellman troca de chaves e implementa os seguintes algoritmos.



| Nome                                   | Uso                | Tipo           | Tamanho da chave (padrão/min/máx.) |
|----------------------------------------|--------------------|----------------|----------------------------|
| Algoritmo de criptografia de mensagem CYLINK    | Criptografia         | Bloquear          | 40/40/40                   |
| DES (padrão de criptografia de dados)         | Criptografia         | Bloquear          | 56/56/56                   |
| Dois DES triplos principais                     | Criptografia         | Bloquear          | 112/112/112                |
| Três teclas DES triplas                   | Criptografia         | Bloquear          | 168/168/168                |
| Algoritmo de troca de chave Diffie-Hellman  | Troca de chaves       | Diffie-Hellman | 512/512/4096               |
| Diffie-Hellman algoritmo efêmero     | Troca de chaves       | Diffie-Hellman | 512/512/4096               |
| Algoritmo de assinatura digital (DSA)      | Assinando            | DSS            | 1024/512/1024              |
| Message Digest 5 (MD5)                 | Hash            | Qualquer            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Criptografia         | Bloquear          | 40/40/128                  |
| RC4 (RSA Data Security 4)              | Criptografia         | Stream         | 40/40/128                  |
| Algoritmo de hash seguro (SHA1)           | Hash            | Qualquer            | 160/160/160                |
| Chave de criptografia Schannel                | Criptografia         | SChannel       | 0/0/-1                     |
| Chave de MAC Schannel                       | Criptografia/hash | SChannel       | 0/0/-1                     |
| Hash do Schannel Master                   | Criptografia/hash | SChannel       | 0/0/-1                     |
| Mestre de protocolo SSL (SSL3)     | Criptografia         | SChannel       | 384/384/384                |
| Mestre de TLS1 (segurança de camada de transporte) | Criptografia         | SChannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Microsoft Enhanced Cryptographic Provider v1.0

Fornece segurança mais forte do que o Microsoft Base Cryptographic Provider v 1.0 usando chaves mais longas com alguns dos algoritmos existentes e implementando algoritmos adicionais.



| Nome                                            | Uso          | Tipo   | Tamanho da chave (padrão/min/máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| DES (padrão de criptografia de dados)                  | Criptografia   | Bloquear  | 56/56/56                   |
| Dois DES triplos principais                              | Criptografia   | Bloquear  | 112/112/112                |
|                                                 | Criptografia   | Bloquear  | 168/168/168                |
| Soma de verificação de autenticação de mensagem com hash (HMAC)   | Hash      | Qualquer    | 0/0/0                      |
| Soma de verificação de autenticação de mensagem (MAC)           | Hash      | Qualquer    | 0/0/0                      |
| Mensagem Digest 2 (MD2)                          | Hash      | Qualquer    | 128/128/128                |
| Mensagem Digest 4 (MD4)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear  | 128/40/128                 |
| RC4 (RSA Data Security 4)                       | Criptografia   | Stream | 128/40/128                 |
| Troca de chaves RSA                                | Troca de chaves | RSA    | 1024/384/16384             |
| Assinatura RSA                                   | Assinando      | RSA    | 1024/384/16384             |
| Algoritmo de hash seguro (SHA1                     | Hash      | Qualquer    | 160/160/160                |
| Secure Socket Layer 3 SHA and MD5 (SSL3 SHAMD5) | Hash      | Qualquer    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS e Diffie-Hellman provedor criptográfico

Fornece segurança mais forte do que o Microsoft Base DSS e Diffie-Hellman CSP do provedor criptográfico usando chaves mais longas com alguns dos algoritmos existentes e implementando algoritmos adicionais.



| Nome                                  | Uso          | Tipo           | Tamanho da chave (padrão/min/máx.) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo de criptografia de mensagem CYLINK   | Criptografia   | Bloquear          | 40/40/40                   |
| DES (padrão de criptografia de dados)        | Criptografia   | Bloquear          | 56/56/56                   |
| Dois DES triplos principais                    | Criptografia   | Bloquear          | 112/112/112                |
| Três teclas DES triplas                  | Criptografia   | Bloquear          | 168/168/168                |
| Algoritmo de troca de chave Diffie-Hellman | Troca de chaves | Diffie-Hellman | 1024/512/4096              |
| Diffie-Hellman algoritmo efêmero    | Troca de chaves | Diffie-Hellman | 1024/512/4096              |
| Algoritmo de assinatura digital (DSA)     | Assinando      | DSS            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hash      | Qualquer            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Criptografia   | Bloquear          | 128/128/128                |
| RC4 (RSA Data Security 4)             | Criptografia   | Stream         | 128/128/128                |
| Algoritmo de hash seguro (SHA1)          | Hash      | Qualquer            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Provedor criptográfico RSA aprimorado da Microsoft e AES

Implementa os seguintes algoritmos para assinar, criptografar e fazer hash de conteúdo.



| Nome                                            | Uso          | Tipo   | Tamanho da chave (padrão/min/máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Criptografia AES 128 (AES128)       | Criptografia   | Bloquear  | 128/128/128                |
| Criptografia AES 192 (AES192)       | Criptografia   | Bloquear  | 192/192/192                |
| Criptografia AES 256 (AES256)       | Criptografia   | Bloquear  | 256/256/256                |
| DES (padrão de criptografia de dados)                  | Criptografia   | Bloquear  | 56/56/56                   |
| Dois DES triplos principais                              | Criptografia   | Bloquear  | 112/112/112                |
| Três teclas DES triplas                            | Criptografia   | Bloquear  | 168/168/168                |
| Soma de verificação de autenticação de mensagem com hash (HMAC)   | Hash      | Qualquer    | 0/0/0                      |
| Soma de verificação de autenticação de mensagem (MAC)           | Hash      | Qualquer    | 0/0/0                      |
| Mensagem Digest 2 (MD2)                          | Hash      | Qualquer    | 128/128/128                |
| Mensagem Digest 4 (MD4)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear  | 128/128/128                |
| RC4 (RSA Data Security 4)                       | Criptografia   | Stream | 128/128/128                |
| Troca de chaves RSA                                | Troca de chaves | RSA    | 1024/384/16384             |
| Assinatura RSA                                   | Assinando      | RSA    | 1024/384/16384             |
| Algoritmo de hash seguro (SHA1)                    | Hash      | Qualquer    | 160/160/160                |
| Algoritmo de hash seguro (SHA256)                  | Hash      | Qualquer    | 256/256/256                |
| Algoritmo de hash seguro (SHA384)                  | Hash      | Qualquer    | 384/384/384                |
| Algoritmo de hash seguro (SHA512)                  | Hash      | Qualquer    | 512/512/512                |
| Secure Socket Layer 3 SHA and MD5 (SSL3 SHAMD5) | Hash      | Qualquer    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Provedor criptográfico do Microsoft RSA Schannel

O oferece suporte ao pacote de segurança do RSA Secure Channel (Schannel) que implementa os protocolos de autenticação protocolo SSL (SSL) e TLS (Transport Layer Security).



| Nome                                            | Uso                | Tipo     | Tamanho da chave (padrão/min/máx.) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| Criptografia AES 128 (AES128)       | Criptografia         | Bloquear    | 128/128/128                |
| Criptografia AES 256 (AES256)       | Criptografia         | Bloquear    | 256/256/256                |
| DES (padrão de criptografia de dados)                  | Criptografia         | Bloquear    | 56/56/56                   |
| Dois DES triplos principais                              | Criptografia         | Bloquear    | 112/112/112                |
| Três teclas DES triplas                            | Criptografia         | Bloquear    | 168/168/168                |
| Soma de verificação de autenticação de mensagem com hash (HMAC)   | Hash            | Qualquer      | 0/0/0                      |
| Soma de verificação de autenticação de mensagem (MAC)           | Hash            | Qualquer      | 0/0/0                      |
| Message Digest 5 (MD5)                          | Hash            | Qualquer      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia         | Bloquear    | 128/128/128                |
| RC4 (RSA Data Security 4)                       | Criptografia         | Stream   | 128/128/128                |
| Troca de chaves RSA                                | Troca de chaves       | RSA      | 1024/384/16384             |
| Chave de criptografia Schannel                         | Criptografia         | SChannel | 0/0/-1                     |
| Hash do Schannel Master                            | Criptografia/hash | SChannel | 0/0/-1                     |
| Chave de MAC Schannel                                | Criptografia/hash | SChannel | 0/0/-1                     |
| Algoritmo de hash seguro (SHA1)                    | Hash            | Qualquer      | 160/160/160                |
| Mestre do SSL2 (Secure Socket Layer 2)             | Criptografia         | SChannel | 40/40/192                  |
| Mestre do SSL3 (Secure Socket Layer 3)             | Criptografia         | SChannel | 384/384/384                |
| Secure Socket Layer 3 SHA and MD5 (SSL3 SHAMD5) | Hash            | Qualquer      | 288/288/288                |
| Mestre de TLS1 (segurança de camada de transporte)          | Criptografia         | SChannel | 384/384/384                |



 

## <a name="microsoft-strong-cryptographic-provider"></a>Microsoft Strong Cryptographic Provider

Implementa os seguintes algoritmos.



| Nome                                            | Uso          | Tipo   | Tamanho da chave (padrão/min/máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| DES (padrão de criptografia de dados)                  | Criptografia   | Bloquear  | 56/56/56                   |
| Dois DES triplos principais                              | Criptografia   | Bloquear  | 112/112/112                |
| Três teclas DES triplas                            | Criptografia   | Bloquear  | 168/168/168                |
| Soma de verificação de autenticação de mensagem com hash (HMAC)   | Hash      | Qualquer    | 0/0/0                      |
| Soma de verificação de autenticação de mensagem (MAC)           | Hash      | Qualquer    | 0/0/0                      |
| Mensagem Digest 2 (MD2)                          | Hash      | Qualquer    | 128/128/128                |
| Mensagem Digest 4 (MD4)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear  | 128/40/128                 |
| RC4 (RSA Data Security 4)                       | Criptografia   | Stream | 128/40/128                 |
| Troca de chaves RSA                                | Troca de chaves | RSA    | 1024/384/16384             |
| Assinatura RSA                                   | Assinando      | RSA    | 1024/384/16384             |
| Algoritmo de hash seguro (SHA1)                    | Hash      | Qualquer    | 160/160/160                |
| Secure Socket Layer 3 SHA and MD5 (SSL3 SHAMD5) | Hash      | Qualquer    | 288/288/288                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre provedores criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
