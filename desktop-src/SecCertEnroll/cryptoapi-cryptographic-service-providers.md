---
description: Os provedores associados à API de Criptografia (CryptoAPI) são chamados de CSPs (provedores de serviços de criptografia) nesta documentação.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Provedores de serviços criptográficos cryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c095fe4801cd57d4665fed0deec1649eb0a64420c13e4e5f486c7afc805447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906576"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Provedores de serviços criptográficos cryptoAPI

Os provedores associados à API de Criptografia ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) são chamados de CSPs (provedores de serviços de criptografia) nesta documentação. Os CSPs normalmente implementam algoritmos criptográficos e fornecem armazenamento de chaves. Os provedores associados ao CNG, por outro lado, separam a implementação do algoritmo do armazenamento de chaves. Os CSPs da Microsoft a seguir são distribuídos com Windows Vista e Windows Server 2008.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Microsoft Base Cryptographic Provider v1.0

Implementa os algoritmos a seguir para hash, assinar e criptografar conteúdo.



| Nome                                            | Usar          | Tipo  | Tamanho da chave (Padrão/Min/Máx.) |
|-------------------------------------------------|--------------|-------|----------------------------|
| DES (Data Encryption Standard)                  | Criptografia   | Bloquear | 56/56/56                   |
| HMAC (Verificação de Autenticação de Mensagem com Hashed)   | Hash      | Qualquer   | 0/0/0                      |
| MAC (Message Authentication Checksum)           | Hash      | Qualquer   | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hash      | Qualquer   | 128/128/128                |
| Message Digest 4 (MD4)                          | Hash      | Qualquer   | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear | 40/40/56                   |
| RSA Data Security 4 (RC4)                       | Criptografia   | Bloquear | 40/40/56                   |
| Chave RSA Exchange                                | Troca de chaves | RSA   | 512/384/1024               |
| Assinatura RSA                                   | Assinando      | RSA   | 512/384/16384              |
| Algoritmo de hash seguro (SHA1)                    | Hash      | Qualquer   | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHIMD5) | Hash      | Qualquer   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Base DSS e Diffie-Hellman criptográfico

Implementa os algoritmos a seguir para dar suporte a hash, assinatura, criptografia e Diffie-Hellman troca de chaves.



| Nome                                  | Usar          | Tipo           | Tamanho da chave (Padrão/Min/Máx.) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo de criptografia de mensagem CYLINK   | Criptografia   | Bloquear          | 40/40/40                   |
| DES (Data Encryption Standard)        | Criptografia   | Bloquear          | 56/56/56                   |
| Diffie-Hellman chave Exchange algoritmo | Troca de chaves | Diffie-Hellman | 512/512/1024               |
| Diffie-Hellman algoritmo efêmero    | Troca de chaves | Diffie-Hellman | 512/512/1024               |
| Algoritmo de Assinatura Digital (DSA)     | Assinando      | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hash      | Qualquer            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Criptografia   | Bloquear          | 40/40/56                   |
| RSA Data Security 4 (RC4)             | Criptografia   | STREAM         | 40/40/56                   |
| Algoritmo de hash seguro (SHA1)          | Hash      | Qualquer            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Microsoft Base DSS Cryptographic Provider

Implementa os seguintes algoritmos para assinar e hash conteúdo:



| Nome                              | Usar     | Tipo | Tamanho da chave (Padrão/Min/Máx.) |
|-----------------------------------|---------|------|----------------------------|
| Algoritmo de Assinatura Digital (DSA) | Assinando | Dss  | 1024/512/1024              |
| Message Digest 5 (MD5)            | Hash | Qualquer  | 128/128/128                |
| Algoritmo de hash seguro (SHA1)      | Hash | Qualquer  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Microsoft Base Smart Card Crypto Provider

Dá suporte a cartões inteligentes e implementa os seguintes algoritmos para hash, assinar e criptografar conteúdo.

| Nome                                            | Usar          | Tipo   | Tamanho da chave (Padrão/Min/Máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| criptografia AES 128 (AES128)       | Criptografia   | Bloquear  | 128/128/128                |
| criptografia AES 192 (AES192)       | Criptografia   | Bloquear  | 192/192/192                |
| criptografia AES 256 (AES256)       | Criptografia   | Bloquear  | 256/256/256                |
| DES (Data Encryption Standard)                  | Criptografia   | Bloquear  | 56/56/56                   |
| DES triplo de duas chaves                              | Criptografia   | Bloquear  | 112/112/112                |
| DES triplo de três chaves                            | Criptografia   | Bloquear  | 168/168/168                |
| HMAC (Verificação de Autenticação de Mensagem com Hashed)   | Hash      | Qualquer    | 0/0/0                      |
| MAC (Message Authentication Checksum)           | Hash      | Qualquer    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Criptografia   | STREAM | 128/40/128                 |
| Chave RSA Exchange                                | Troca de chaves | RSA    | 1024/1024/4096             |
| Assinatura RSA                                   | Assinando      | RSA    | 1024/1024/4096             |
| Algoritmo de hash seguro (SHA1)                    | Hash      | Qualquer    | 160/160/160                |
| Algoritmo de hash seguro 256 (SHA256)              | Hash      | Qualquer    | 256/256/256                |
| Algoritmo de hash seguro 384 (SHA384)              | Hash      | Qualquer    | 384/384/384                |
| Algoritmo de hash seguro 512 (SHA512)              | Hash      | Qualquer    | 512/512/512                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHIMD5) | Hash      | Qualquer    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Provedor criptográfico do Microsoft DH Schannel

Dá suporte ao pacote de segurança Schannel (Canal Seguro), que implementa protocolos de autenticação protocolo SSL (SSL) e TLS (Transport Layer Security). Esse CSP também dá suporte Diffie-Hellman troca de chaves e implementa os algoritmos a seguir.



| Nome                                   | Usar                | Tipo           | Tamanho da chave (Padrão/Min/Máx.) |
|----------------------------------------|--------------------|----------------|----------------------------|
| Algoritmo de criptografia de mensagem CYLINK    | Criptografia         | Bloquear          | 40/40/40                   |
| DES (Data Encryption Standard)         | Criptografia         | Bloquear          | 56/56/56                   |
| DES triplo de duas chaves                     | Criptografia         | Bloquear          | 112/112/112                |
| DES triplo de três chaves                   | Criptografia         | Bloquear          | 168/168/168                |
| Diffie-Hellman algoritmo de Exchange chave  | Troca de chaves       | Diffie-Hellman | 512/512/4096               |
| Diffie-Hellman algoritmo efêmero     | Troca de chaves       | Diffie-Hellman | 512/512/4096               |
| Algoritmo de Assinatura Digital (DSA)      | Assinando            | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                 | Hash            | Qualquer            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Criptografia         | Bloquear          | 40/40/128                  |
| RSA Data Security 4 (RC4)              | Criptografia         | STREAM         | 40/40/128                  |
| Algoritmo de hash seguro (SHA1)           | Hash            | Qualquer            | 160/160/160                |
| Chave de criptografia Schannel                | Criptografia         | SChannel       | 0/0/-1                     |
| Chave MAC Schannel                       | Criptografia/hash | SChannel       | 0/0/-1                     |
| Hash mestre Schannel                   | Criptografia/hash | SChannel       | 0/0/-1                     |
| protocolo SSL (SSL3) Mestre     | Criptografia         | SChannel       | 384/384/384                |
| TLS1 (Transport Layer Security) Master | Criptografia         | SChannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Microsoft Enhanced Cryptographic Provider v1.0

Fornece segurança mais forte do que o Microsoft Base Cryptographic Provider v1.0 usando chaves mais longas com alguns dos algoritmos existentes e implementando algoritmos adicionais.



| Nome                                            | Usar          | Tipo   | Tamanho da chave (Padrão/Min/Máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| DES (Data Encryption Standard)                  | Criptografia   | Bloquear  | 56/56/56                   |
| DES triplo de duas chaves                              | Criptografia   | Bloquear  | 112/112/112                |
|                                                 | Criptografia   | Bloquear  | 168/168/168                |
| HMAC (Verificação de Autenticação de Mensagem com Hashed)   | Hash      | Qualquer    | 0/0/0                      |
| MAC (Message Authentication Checksum)           | Hash      | Qualquer    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Criptografia   | STREAM | 128/40/128                 |
| Chave RSA Exchange                                | Troca de chaves | RSA    | 1024/384/16384             |
| Assinatura RSA                                   | Assinando      | RSA    | 1024/384/16384             |
| Algoritmo de hash seguro (SHA1)                     | Hash      | Qualquer    | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHIMD5) | Hash      | Qualquer    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS e Diffie-Hellman Cryptographic Provider

Fornece segurança mais forte do que o CSP do Provedor criptográfico do Microsoft Base DSS e Diffie-Hellman usando chaves mais longas com alguns dos algoritmos existentes e implementando algoritmos adicionais.



| Nome                                  | Usar          | Tipo           | Tamanho da chave (Padrão/Min/Máx.) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo de criptografia de mensagem CYLINK   | Criptografia   | Bloquear          | 40/40/40                   |
| DES (Data Encryption Standard)        | Criptografia   | Bloquear          | 56/56/56                   |
| DES triplo de duas chaves                    | Criptografia   | Bloquear          | 112/112/112                |
| DES triplo de três chaves                  | Criptografia   | Bloquear          | 168/168/168                |
| Diffie-Hellman algoritmo de Exchange chave | Troca de chaves | Diffie-Hellman | 1024/512/4096              |
| Diffie-Hellman algoritmo efêmero    | Troca de chaves | Diffie-Hellman | 1024/512/4096              |
| Algoritmo de Assinatura Digital (DSA)     | Assinando      | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hash      | Qualquer            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Criptografia   | Bloquear          | 128/128/128                |
| RSA Data Security 4 (RC4)             | Criptografia   | STREAM         | 128/128/128                |
| Algoritmo de hash seguro (SHA1)          | Hash      | Qualquer            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Provedor criptográfico AES e RSA aprimorado da Microsoft

Implementa os algoritmos a seguir para assinar, criptografar e hash conteúdo.



| Nome                                            | Usar          | Tipo   | Tamanho da chave (Padrão/Min/Máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| criptografia AES 128 (AES128)       | Criptografia   | Bloquear  | 128/128/128                |
| criptografia AES 192 (AES192)       | Criptografia   | Bloquear  | 192/192/192                |
| criptografia AES 256 (AES256)       | Criptografia   | Bloquear  | 256/256/256                |
| DES (Data Encryption Standard)                  | Criptografia   | Bloquear  | 56/56/56                   |
| DES triplo de duas chaves                              | Criptografia   | Bloquear  | 112/112/112                |
| DES triplo de três chaves                            | Criptografia   | Bloquear  | 168/168/168                |
| HMAC (Verificação de Autenticação de Mensagem com Hashed)   | Hash      | Qualquer    | 0/0/0                      |
| MAC (Message Authentication Checksum)           | Hash      | Qualquer    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hash      | Qualquer    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hash      | Qualquer    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia   | Bloquear  | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Criptografia   | STREAM | 128/128/128                |
| Chave RSA Exchange                                | Troca de chaves | RSA    | 1024/384/16384             |
| Assinatura RSA                                   | Assinando      | RSA    | 1024/384/16384             |
| Algoritmo de hash seguro (SHA1)                    | Hash      | Qualquer    | 160/160/160                |
| Algoritmo de hash seguro (SHA256)                  | Hash      | Qualquer    | 256/256/256                |
| Algoritmo de hash seguro (SHA384)                  | Hash      | Qualquer    | 384/384/384                |
| Algoritmo de hash seguro (SHA512)                  | Hash      | Qualquer    | 512/512/512                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHIMD5) | Hash      | Qualquer    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Provedor criptográfico Microsoft RSA Schannel

Dá suporte ao pacote de segurança rsa secure channel (Schannel) que implementa protocolos de autenticação protocolo SSL (SSL) e TLS (Transport Layer Security).



| Nome                                            | Usar                | Tipo     | Tamanho da chave (Padrão/Min/Máx.) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| criptografia AES 128 (AES128)       | Criptografia         | Bloquear    | 128/128/128                |
| criptografia AES 256 (AES256)       | Criptografia         | Bloquear    | 256/256/256                |
| DES (Data Encryption Standard)                  | Criptografia         | Bloquear    | 56/56/56                   |
| DES triplo de duas chaves                              | Criptografia         | Bloquear    | 112/112/112                |
| DES triplo de três chaves                            | Criptografia         | Bloquear    | 168/168/168                |
| Soma de verificação de autenticação de mensagem com hash (HMAC)   | Hash            | Qualquer      | 0/0/0                      |
| Soma de verificação de autenticação de mensagem (MAC)           | Hash            | Qualquer      | 0/0/0                      |
| Message Digest 5 (MD5)                          | Hash            | Qualquer      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Criptografia         | Bloquear    | 128/128/128                |
| RC4 (RSA Data Security 4)                       | Criptografia         | STREAM   | 128/128/128                |
| Exchange de chave RSA                                | Troca de chaves       | RSA      | 1024/384/16384             |
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



| Nome                                            | Usar          | Tipo   | Tamanho da chave (padrão/min/máx.) |
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
| RC4 (RSA Data Security 4)                       | Criptografia   | STREAM | 128/40/128                 |
| Chave RSA Exchange                                | Troca de chaves | RSA    | 1024/384/16384             |
| Assinatura RSA                                   | Assinando      | RSA    | 1024/384/16384             |
| Algoritmo de hash seguro (SHA1)                    | Hash      | Qualquer    | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHIMD5) | Hash      | Qualquer    | 288/288/288                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre provedores criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
