---
description: Especifica um identificador de algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762909"
---
# <a name="alg_id"></a>ALG_ID

O tipo de dados **ALG_ID** especifica um identificador de algoritmo. Os parâmetros desse tipo de dados são passados para a maioria das funções no CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



A tabela a seguir lista os identificadores de algoritmo que estão definidos no momento. Os autores de CSPs ( [*provedores de serviços de criptografia*](../secgloss/c-gly.md) ) personalizados podem definir novos valores. Além disso, o **ALG_ID** usado por CSPs personalizados para as principais especificações **AT_KEYEXCHANGE** e **AT_SIGNATURE** são dependentes do provedor. Os mapeamentos atuais seguem a tabela.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificador</th>
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CALG_3DES</td>
<td>0x00006603</td>
<td>Algoritmo de criptografia <a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> .</td>
</tr>
<tr class="even">
<td>CALG_3DES_112</td>
<td>0x00006609</td>
<td>Criptografia <a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> de duas chaves com comprimento de chave efetivo igual a 112 bits.</td>
</tr>
<tr class="odd">
<td>CALG_AES</td>
<td>0x00006611</td>
<td>Criptografia AES (AES). Esse algoritmo é compatível com o <a href="microsoft-aes-cryptographic-provider.md">provedor criptográfico do Microsoft AES</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_128</td>
<td>0x0000660e</td>
<td>AES de 128 bits. Esse algoritmo é compatível com o <a href="microsoft-aes-cryptographic-provider.md">provedor criptográfico do Microsoft AES</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AES_192</td>
<td>0x0000660f</td>
<td>AES de 192 bits. Esse algoritmo é compatível com o <a href="microsoft-aes-cryptographic-provider.md">provedor criptográfico do Microsoft AES</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_256</td>
<td>0x00006610</td>
<td>AES de 256 bits. Esse algoritmo é compatível com o <a href="microsoft-aes-cryptographic-provider.md">provedor criptográfico do Microsoft AES</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AGREEDKEY_ANY</td>
<td>0x0000aa03</td>
<td>Identificador de algoritmo temporário para identificadores do Diffie-Hellman – chaves acordadas.</td>
</tr>
<tr class="even">
<td>CALG_CYLINK_MEK</td>
<td>0x0000660c</td>
<td>Um algoritmo para criar uma chave DES de 40 bits que tem bits de paridade e bits de chave zerados para tornar seu comprimento de chave 64 bits. Esse algoritmo é compatível com o <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="odd">
<td>CALG_DES</td>
<td>0x00006601</td>
<td>Algoritmo de criptografia DES.</td>
</tr>
<tr class="even">
<td>CALG_DESX</td>
<td>0x00006604</td>
<td>Algoritmo de criptografia DESX.</td>
</tr>
<tr class="odd">
<td>CALG_DH_EPHEM</td>
<td>0x0000aa02</td>
<td>Diffie-Hellman algoritmo de troca de chave efêmera.</td>
</tr>
<tr class="even">
<td>CALG_DH_SF</td>
<td>0x0000aa01</td>
<td>Diffie-Hellman armazenar e encaminhar o algoritmo de troca de chaves.</td>
</tr>
<tr class="odd">
<td>CALG_DSS_SIGN</td>
<td>0x00002200</td>
<td>Algoritmo de assinatura de <a href="/windows/desktop/SecGloss/p-gly"><em>chave pública</em></a> DSA.</td>
</tr>
<tr class="even">
<td>CALG_ECDH</td>
<td>0x0000aa05</td>
<td>Curva elíptica Diffie-Hellman algoritmo de troca de chaves.
<blockquote>
[!Note]<br />
Esse algoritmo tem suporte apenas por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de criptografia: próxima geração</a>.
</blockquote>
<br/> <strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECDH_EPHEM</td>
<td>0x0000ae06</td>
<td>Curva elíptica efêmera Diffie-Hellman algoritmo de troca de chaves.
<blockquote>
[!Note]<br />
Esse algoritmo tem suporte apenas por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de criptografia: próxima geração</a>.
</blockquote>
<br/> <strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.<br/></td>
</tr>
<tr class="even">
<td>CALG_ECDSA</td>
<td>0x00002203</td>
<td>Algoritmo de assinatura digital de curva elíptica.
<blockquote>
[!Note]<br />
Esse algoritmo tem suporte apenas por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de criptografia: próxima geração</a>.
</blockquote>
<br/> <strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECMQV</td>
<td>0x0000a001</td>
<td>Algoritmo de troca de chave Menezes, t e Vanstone (MQV) de curva elíptica. Não há suporte para esse algoritmo.</td>
</tr>
<tr class="even">
<td>CALG_HASH_REPLACE_OWF</td>
<td>0x0000800b</td>
<td>Algoritmo de hash de função unidirecional.</td>
</tr>
<tr class="odd">
<td>CALG_HUGHES_MD5</td>
<td>0x0000a003</td>
<td>Algoritmo de hash MD5 Hughes.</td>
</tr>
<tr class="even">
<td>CALG_HMAC</td>
<td>0x00008009</td>
<td>Algoritmo de hash com chave HMAC. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="odd">
<td>CALG_KEA_KEYX</td>
<td>0x0000aa04</td>
<td>FORTEZZA (KEA Key Exchange Algorithm). Não há suporte para esse algoritmo.</td>
</tr>
<tr class="even">
<td>CALG_MAC</td>
<td>0x00008005</td>
<td>Algoritmo de hash com chave <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> . Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="odd">
<td>CALG_MD2</td>
<td>0x00008001</td>
<td>Algoritmo de hash MD2. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="even">
<td>CALG_MD4</td>
<td>0x00008002</td>
<td>Algoritmo de hash MD4.</td>
</tr>
<tr class="odd">
<td>CALG_MD5</td>
<td>0x00008003</td>
<td>Algoritmo de hash MD5. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="even">
<td>CALG_NO_SIGN</td>
<td>0x00002000</td>
<td>Nenhum algoritmo de assinatura.</td>
</tr>
<tr class="odd">
<td>CALG_OID_INFO_CNG_ONLY</td>
<td>0xFFFFFFFF</td>
<td>O algoritmo é implementado apenas na CNG. A macro, IS_SPECIAL_OID_INFO_ALGID, pode ser usada para determinar se um algoritmo de criptografia tem suporte apenas usando as funções CNG.</td>
</tr>
<tr class="even">
<td>CALG_OID_INFO_PARAMETERS</td>
<td>0xfffffffe</td>
<td>O algoritmo é definido nos parâmetros codificados. O algoritmo só tem suporte usando o CNG. A macro, IS_SPECIAL_OID_INFO_ALGID, pode ser usada para determinar se um algoritmo de criptografia tem suporte apenas usando as funções CNG.</td>
</tr>
<tr class="odd">
<td>CALG_PCT1_MASTER</td>
<td>0x00004c04</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
<tr class="even">
<td>CALG_RC2</td>
<td>0x00006602</td>
<td>Algoritmo de criptografia de bloco RC2. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="odd">
<td>CALG_RC4</td>
<td>0x00006801</td>
<td>Algoritmo de criptografia de fluxo RC4. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="even">
<td>CALG_RC5</td>
<td>0x0000660d</td>
<td>Algoritmo de criptografia de bloco RC5.</td>
</tr>
<tr class="odd">
<td>CALG_RSA_KEYX</td>
<td>0x0000a400</td>
<td>Algoritmo de troca de chave pública RSA. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="even">
<td>CALG_RSA_SIGN</td>
<td>0x00002400</td>
<td>Algoritmo de assinatura de chave pública RSA. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_ENC_KEY</td>
<td>0x00004c07</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
<tr class="even">
<td>CALG_SCHANNEL_MAC_KEY</td>
<td>0x00004c03</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_MASTER_HASH</td>
<td>0x00004c02</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
<tr class="even">
<td>CALG_SEAL</td>
<td>0x00006802</td>
<td>Algoritmo de criptografia do lacre. Não há suporte para esse algoritmo.</td>
</tr>
<tr class="odd">
<td>CALG_SHA</td>
<td>0x00008004</td>
<td>Algoritmo de hash SHA. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="even">
<td>CALG_SHA1</td>
<td>0x00008004</td>
<td>O mesmo que <strong>CALG_SHA</strong>. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SHA_256</td>
<td>0x0000800c</td>
<td>algoritmo de hash SHA de 256 bits. Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).<br/> <strong>Windows XP com SP2, Windows XP com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.<br/></td>
</tr>
<tr class="even">
<td>CALG_SHA_384</td>
<td>0x0000800d</td>
<td>algoritmo de hash SHA de 384 bits. Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).<br/> <strong>Windows XP com SP2, Windows XP com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.<br/></td>
</tr>
<tr class="odd">
<td>CALG_SHA_512</td>
<td>0x0000800e</td>
<td>algoritmo de hash SHA de 512 bits. Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).<br/> <strong>Windows XP com SP2, Windows XP com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.<br/></td>
</tr>
<tr class="even">
<td>CALG_SKIPJACK</td>
<td>0x0000660a</td>
<td>Skipjack o algoritmo de criptografia de bloco (FORTEZZA). Não há suporte para esse algoritmo.</td>
</tr>
<tr class="odd">
<td>CALG_SSL2_MASTER</td>
<td>0x00004c05</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
<tr class="even">
<td>CALG_SSL3_MASTER</td>
<td>0x00004c01</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
<tr class="odd">
<td>CALG_SSL3_SHAMD5</td>
<td>0x00008008</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
<tr class="even">
<td>CALG_TEK</td>
<td>0x0000660b</td>
<td>TEK (FORTEZZA). Não há suporte para esse algoritmo.</td>
</tr>
<tr class="odd">
<td>CALG_TLS1_MASTER</td>
<td>0x00004c06</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
<tr class="even">
<td>CALG_TLS1PRF</td>
<td>0x0000800a</td>
<td>Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</td>
</tr>
</tbody>
</table>



 

Para o [provedor criptográfico base da Microsoft](microsoft-base-cryptographic-provider.md), o [provedor de criptografia forte da Microsoft](microsoft-strong-cryptographic-provider.md)e o [provedor criptográfico aprimorado](microsoft-enhanced-cryptographic-provider.md)da Microsoft, os **ALG_IDs** usados para as principais especificações **AT_KEYEXCHANGE** e **AT_SIGNATURE** são os seguintes:

-   **CALG_RSA_KEYX** é usado para **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** é usado para **AT_SIGNATURE**.

Para o [Microsoft Base DSS e o provedor de criptografia Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), os **ALG_IDs** usados para as principais especificações **AT_KEYEXCHANGE** e **AT_SIGNATURE** são os seguintes:

-   **CALG_DH_SF** é usado para **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** é usado para **AT_SIGNATURE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de criptografia](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
