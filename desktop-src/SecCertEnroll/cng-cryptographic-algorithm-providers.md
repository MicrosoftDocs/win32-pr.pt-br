---
description: 'Ao contrário da API de Criptografia (CryptoAPI), a API de Criptografia: CNG (Próxima Geração) separa os provedores criptográficos dos provedores de armazenamento de chaves.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Provedores de algoritmo criptográfico CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fd98a7eb6fd159c54977cdf8b72ebffd747da48
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467072"
---
# <a name="cng-cryptographic-algorithm-providers"></a>Provedores de algoritmo criptográfico CNG

Ao contrário da API de Criptografia (CryptoAPI), a API de Criptografia: CNG (Próxima Geração) separa os provedores criptográficos dos provedores de armazenamento de chaves. Operações básicas de algoritmo criptográfico, como hash e assinatura, são chamadas de operações primitivas ou simplesmente primitivos. O CNG inclui um provedor que implementa os algoritmos a seguir.

-   [Algoritmos simétricos](#symmetric-algorithms)
-   [Algoritmos assimétricos](#asymmetric-algorithms)
-   [Algoritmos de hash](#hashing-algorithms)
-   [Algoritmos Exchange chave](#key-exchange-algorithms)
-   [Tópicos relacionados](#related-topics)

## <a name="symmetric-algorithms"></a>Algoritmos simétricos



| Nome                                   | Modos com suporte                                                                                                                                                                                                 | Tamanho da chave em bits (Default/Min/Max) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| AES (criptografia AES)     | ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS<br/> **Windows 8:** O suporte para os modos CFB128 e CMAC começa.<br/> **Windows 10:** O suporte para o modo XTS-AES começa.<br/> | 128/192/256                        |
| DES (Data Encryption Standard)         | ECB, CBC, CFB8, CFB64<br/> **Windows 8:** O suporte para o modo CFB64 começa.<br/>                                                                                                                   | 56/56/56                           |
| Data Encryption Standard XORed(DESX)   | ECB, CBC, CFB8, CFB64 <br/> **Windows 8:** O suporte para o modo CFB64 começa.<br/>                                                                                                                  | 192/192/192                        |
| 3DES (Triple Data Encryption Standard) | ECB, CBC, CFB8, CFB64 <br/> **Windows 8:** O suporte para o modo CFB64 começa.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | Há suporte para os modos ECB, CBC, CFB8, CFB64.<br/> **Windows 8:** O suporte para o modo CFB64 começa.<br/>                                                                                              | 16 a 128 em incrementos de 8 bits      |
| RSA Data Security 4 (RC4)              |                                                                                                                                                                                                                 | 8 a 512, em incrementos de 8 bits      |



 

## <a name="asymmetric-algorithms"></a>Algoritmos assimétricos



| Nome                              | Observações                                                                                                                                                                             | Tamanho da chave em bits (Default/Min/Max)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Algoritmo de Assinatura Digital (DSA) | A implementação está em conformidade com o FIPS 186-3 para tamanhos de chave entre 1024 e 3072 bits. <br/> A implementação está em conformidade com o FIPS 186-2 para tamanhos de chave de 512 a 1024 bits.<br/> | 512 a 3072, em incrementos de 64 bits<br/> **Windows 8:** O suporte para uma chave de 3072 bits começa.<br/> |
| RSA                               | Inclui algoritmos RSA que usam PKCS1, codificação ou preenchimento de OAEP (Preenchimento de Criptografia Assimétrica Ideal) ou preenchimento de texto não criptografado do PSS (Esquema de Assinatura Probabilística)               | 512 a 16384, em incrementos de 64 bits                                                                            |



 

## <a name="hashing-algorithms"></a>Algoritmos de hash



| Nome                               | Observações               | Tamanho da chave em bits (Default/Min/Max) |
|------------------------------------|---------------------|------------------------------------|
| Secure Hash Algorithm 1 (SHA1)     | Inclui HmacSha1   | 160/160/160                        |
| Algoritmo de hash seguro 256 (SHA256) | Inclui HmacSha256 | 256/256/256                        |
| Algoritmo de hash seguro 384 (SHA384) | Inclui HmacSha384 | 384/384/384                        |
| Algoritmo de hash seguro 512 (SHA512) | Inclui HmacSha512 | 512/512/512                        |
| Message Digest 2 (MD2)             | Inclui HmacMd2    | 128/128/128                        |
| Message Digest 4 (MD4)             | Inclui HmacMd4    | 128/128/128                        |
| Message Digest 5 (MD5)             | Inclui HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Algoritmos Exchange chave




| Nome do algoritmo | Observações | Tamanho da chave em bits (Default/Min/Max) | 
|----------------|-------|------------------------------------|
| Diffie-Hellman algoritmo de Exchange chave | 512 a 4096, em incrementos de 64 bits | 
| EcDH (Diffie-Hellman curva elíptica) | Inclui curvas que usam chaves públicas de 256, 384 e 521 bits, conforme especificado em SP800-56A. | 256/384/521 | 
| Algoritmo de assinatura digital de curva elíptica (ECDSA) | Inclui curvas que usam chaves públicas de 256, 384 e 521 bits, conforme especificado em FIPS 186-3.<blockquote>[!Note]<br />Para exibir todas as curvas elípticas nomeadas, use <strong>certutil displayEccCurve.</strong></blockquote><br /> | 256/384/521 | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funções primitivas criptográficas CNG](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Noções básicas sobre provedores criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

