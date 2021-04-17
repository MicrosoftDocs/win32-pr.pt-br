---
description: 'Ao contrário da CryptoAPI (API de criptografia), a CNG (API de criptografia: próxima geração) separa os provedores criptográficos dos principais provedores de armazenamento.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Provedores de algoritmos criptográficos CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748661"
---
# <a name="cng-cryptographic-algorithm-providers"></a>Provedores de algoritmos criptográficos CNG

Ao contrário da CryptoAPI (API de criptografia), a CNG (API de criptografia: próxima geração) separa os provedores criptográficos dos principais provedores de armazenamento. As operações básicas do algoritmo de criptografia, como hash e assinatura, são chamadas de operações primitivas ou simplesmente primitivos. A CNG inclui um provedor que implementa os seguintes algoritmos.

-   [Algoritmos simétricos](#symmetric-algorithms)
-   [Algoritmos assimétricos](#asymmetric-algorithms)
-   [Algoritmos de hash](#hashing-algorithms)
-   [Algoritmos de troca de chaves](#key-exchange-algorithms)
-   [Tópicos relacionados](#related-topics)

## <a name="symmetric-algorithms"></a>Algoritmos simétricos



| Nome                                   | Modos com suporte                                                                                                                                                                                                 | Tamanho da chave em bits (padrão/mín/máx.) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| AES (criptografia AES)     | ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, encapsulamento de chave AES, XTS<br/> **Windows 8:** O suporte para os modos CFB128 e CMAC começa.<br/> **Windows 10:** O suporte para o modo XTS-AES é iniciado.<br/> | 128/192/256                        |
| DES (padrão de criptografia de dados)         | ECB, CBC, CFB8, CFB64<br/> **Windows 8:** O suporte para o modo CFB64 começa.<br/>                                                                                                                   | 56/56/56                           |
| XORed padrão de criptografia de dados (DESX)   | ECB, CBC, CFB8, CFB64 <br/> **Windows 8:** O suporte para o modo CFB64 começa.<br/>                                                                                                                  | 192/192/192                        |
| 3DES (padrão de criptografia de dados triplo) | ECB, CBC, CFB8, CFB64 <br/> **Windows 8:** O suporte para o modo CFB64 começa.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | Há suporte para os modos ECB, CBC, CFB8, CFB64.<br/> **Windows 8:** O suporte para o modo CFB64 começa.<br/>                                                                                              | 16 a 128 em incrementos de 8 bits      |
| RC4 (RSA Data Security 4)              |                                                                                                                                                                                                                 | 8 a 512, em incrementos de 8 bits      |



 

## <a name="asymmetric-algorithms"></a>Algoritmos assimétricos



| Nome                              | Observações                                                                                                                                                                             | Tamanho da chave em bits (padrão/mín/máx.)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Algoritmo de assinatura digital (DSA) | A implementação está de acordo com o FIPS 186-3 para os tamanhos de chave entre 1024 e 3072 bits. <br/> A implementação está de acordo com o FIPS 186-2 para os tamanhos de chave de 512 a 1024 bits.<br/> | 512 a 3072, em incrementos de bits 64<br/> **Windows 8:** O suporte para a chave de 3072 bits começa.<br/> |
| RSA                               | Inclui algoritmos RSA que usam PKCS1, codificação ou preenchimento da OAEP (preenchimento de criptografia assimétrica) ideal ou preenchimento de texto não criptografado do PSS (esquema de assinatura probabilística)               | 512 a 16384, em incrementos de bits 64                                                                            |



 

## <a name="hashing-algorithms"></a>Algoritmos de hash



| Nome                               | Observações               | Tamanho da chave em bits (padrão/mín/máx.) |
|------------------------------------|---------------------|------------------------------------|
| Secure Hash Algorithm 1 (SHA1)     | Inclui HmacSha1   | 160/160/160                        |
| Algoritmo de hash seguro 256 (SHA256) | Inclui HmacSha256 | 256/256/256                        |
| Algoritmo de hash seguro 384 (SHA384) | Inclui HmacSha384 | 384/384/384                        |
| Algoritmo de hash seguro 512 (SHA512) | Inclui HmacSha512 | 512/512/512                        |
| Mensagem Digest 2 (MD2)             | Inclui HmacMd2    | 128/128/128                        |
| Mensagem Digest 4 (MD4)             | Inclui HmacMd4    | 128/128/128                        |
| Message Digest 5 (MD5)             | Inclui HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Algoritmos de troca de chaves



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome do algoritmo</th>
<th>Observações</th>
<th>Tamanho da chave em bits (padrão/mín/máx.)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Algoritmo de troca de chave Diffie-Hellman</td>

<td>512 a 4096, em incrementos de bits 64</td>
</tr>
<tr class="even">
<td>Diffie-Hellman de curva elíptica (ECDH)</td>
<td>Inclui curvas que usam chaves públicas 256, 384 e 521 bits, conforme especificado em SP800-56A.</td>
<td>256/384/521</td>
</tr>
<tr class="odd">
<td>ECDSA (algoritmo de assinatura digital de curva elíptica)</td>
<td>Inclui curvas que usam chaves públicas 256, 384 e 521 bits, conforme especificado no FIPS 186-3.
<blockquote>
[!Note]<br />
Para exibir todas as curvas elípticas nomeadas, use <strong>certutil displayEccCurve</strong>.
</blockquote>
<br/></td>
<td>256/384/521</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funções primitivas de criptografia CNG](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Noções básicas sobre provedores criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

