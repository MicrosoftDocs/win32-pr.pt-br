---
description: Especifica um identificador de algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f4b6c476a8ea6e61785a096abf33c357d9b024
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482392"
---
# <a name="alg_id"></a>ALG_ID

O **ALG_ID** de dados especifica um identificador de algoritmo. Os parâmetros desse tipo de dados são passados para a maioria das funções em CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



A tabela a seguir lista os identificadores de algoritmo que estão definidos no momento. Os autores de [*CSPs (provedores de serviços criptográficos) personalizados*](../secgloss/c-gly.md) podem definir novos valores. Além disso, **as ALG_ID** usadas por CSPs personalizados para as especificações de **chave AT_KEYEXCHANGE** **e** AT_SIGNATURE são dependentes do provedor. Os mapeamentos atuais seguem a tabela.




| Identificador | Valor | Descrição | 
|------------|-------|-------------|
| CALG_3DES | 0x00006603 | <a href="/windows/desktop/SecGloss/t-gly"><em>Algoritmo de criptografia DES</em></a> triplo. | 
| CALG_3DES_112 | 0x00006609 | Criptografia <a href="/windows/desktop/SecGloss/t-gly"><em>DES triplo de duas</em></a> chaves com comprimento efetivo de chave igual a 112 bits. | 
| CALG_AES | 0x00006611 | criptografia AES (AES). Esse algoritmo é suportado pelo Provedor criptográfico <a href="microsoft-aes-cryptographic-provider.md">do Microsoft AES.</a> | 
| CALG_AES_128 | 0x0000660e | AES de 128 bits. Esse algoritmo é suportado pelo Provedor criptográfico <a href="microsoft-aes-cryptographic-provider.md">do Microsoft AES.</a> | 
| CALG_AES_192 | 0x0000660f | AES de 192 bits. Esse algoritmo é suportado pelo Provedor criptográfico <a href="microsoft-aes-cryptographic-provider.md">do Microsoft AES.</a> | 
| CALG_AES_256 | 0x00006610 | AES de 256 bits. Esse algoritmo é suportado pelo Provedor criptográfico <a href="microsoft-aes-cryptographic-provider.md">do Microsoft AES.</a> | 
| CALG_AGREEDKEY_ANY | 0x0000aa03 | Identificador de algoritmo temporário para identificadores de chaves de acordo com Diffie-Hellman. | 
| CALG_CYLINK_MEK | 0x0000660c | Um algoritmo para criar uma chave DES de 40 bits que tem bits de paridade e bits de chave zero para tornar seu comprimento de chave de 64 bits. Esse algoritmo é suportado pelo Provedor <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">criptográfico base da Microsoft.</a> | 
| CALG_DES | 0x00006601 | Algoritmo de criptografia DES. | 
| CALG_DESX | 0x00006604 | Algoritmo de criptografia DESX. | 
| CALG_DH_EPHEM | 0x0000aa02 | Diffie-Hellman algoritmo de troca de chaves efêmeras. | 
| CALG_DH_SF | 0x0000aa01 | Diffie-Hellman armazenar e encaminhar o algoritmo de troca de chaves. | 
| CALG_DSS_SIGN | 0x00002200 | Algoritmo de assinatura <a href="/windows/desktop/SecGloss/p-gly"><em>de chave pública DSA.</em></a> | 
| CALG_ECDH | 0x0000aa05 | Curva elíptica Diffie-Hellman algoritmo de troca de chaves.<blockquote>[!Note]<br />Esse algoritmo só tem suporte por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de Criptografia: Próxima Geração.</a></blockquote><br /><strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.<br /> | 
| CALG_ECDH_EPHEM | 0x0000ae06 | Curva elíptica efêmera Diffie-Hellman algoritmo de troca de chaves.<blockquote>[!Note]<br />Esse algoritmo só tem suporte por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de Criptografia: Próxima Geração.</a></blockquote><br /><strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.<br /> | 
| CALG_ECDSA | 0x00002203 | Algoritmo de assinatura digital de curva elíptica.<blockquote>[!Note]<br />Esse algoritmo só tem suporte por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de Criptografia: Próxima Geração.</a></blockquote><br /><strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.<br /> | 
| CALG_ECMQV | 0x0000a001 | Algoritmo de troca de chaves MQV (Meticaes, Qu e Vanstone) de curva elíptica. Não há suporte para esse algoritmo. | 
| CALG_HASH_REPLACE_OWF | 0x0000800b | Algoritmo de hash de função de uma maneira. | 
| CALG_HUGHES_MD5 | 0x0000a003 | Algoritmo de hash MD5 de MD5. | 
| CALG_HMAC | 0x00008009 | Algoritmo de hash com chave HMAC. Esse algoritmo é suportado pelo Provedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base da Microsoft.</a> | 
| CALG_KEA_KEYX | 0x0000aa04 | Algoritmo de troca de chaves KEA (FORTEZZA). Não há suporte para esse algoritmo. | 
| CALG_MAC | 0x00008005 | Algoritmo de hash com chave <a href="/windows/desktop/SecGloss/m-gly"><em>MAC.</em></a> Esse algoritmo é suportado pelo Provedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base da Microsoft.</a> | 
| CALG_MD2 | 0x00008001 | Algoritmo de hash MD2. Esse algoritmo é suportado pelo Provedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base da Microsoft.</a> | 
| CALG_MD4 | 0x00008002 | Algoritmo de hash MD4. | 
| CALG_MD5 | 0x00008003 | Algoritmo de hash MD5. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>. | 
| CALG_NO_SIGN | 0x00002000 | Nenhum algoritmo de assinatura. | 
| CALG_OID_INFO_CNG_ONLY | 0xffffffff | O algoritmo é implementado apenas na CNG. A macro, IS_SPECIAL_OID_INFO_ALGID, pode ser usada para determinar se um algoritmo de criptografia tem suporte apenas usando as funções CNG. | 
| CALG_OID_INFO_PARAMETERS | 0xfffffffe | O algoritmo é definido nos parâmetros codificados. O algoritmo só tem suporte usando o CNG. A macro, IS_SPECIAL_OID_INFO_ALGID, pode ser usada para determinar se um algoritmo de criptografia tem suporte apenas usando as funções CNG. | 
| CALG_PCT1_MASTER | 0x00004c04 | Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 
| CALG_RC2 | 0x00006602 | Algoritmo de criptografia de bloco RC2. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>. | 
| CALG_RC4 | 0x00006801 | Algoritmo de criptografia de fluxo RC4. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>. | 
| CALG_RC5 | 0x0000660d | Algoritmo de criptografia de bloco RC5. | 
| CALG_RSA_KEYX | 0x0000a400 | Algoritmo de troca de chave pública RSA. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>. | 
| CALG_RSA_SIGN | 0x00002400 | Algoritmo de assinatura de chave pública RSA. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>. | 
| CALG_SCHANNEL_ENC_KEY | 0x00004c07 | Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 
| CALG_SCHANNEL_MAC_KEY | 0x00004c03 | Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 
| CALG_SCHANNEL_MASTER_HASH | 0x00004c02 | Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 
| CALG_SEAL | 0x00006802 | Algoritmo de criptografia do lacre. Não há suporte para esse algoritmo. | 
| CALG_SHA | 0x00008004 | Algoritmo de hash SHA. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>. | 
| CALG_SHA1 | 0x00008004 | O mesmo que <strong>CALG_SHA</strong>. Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>. | 
| CALG_SHA_256 | 0x0000800c | algoritmo de hash SHA de 256 bits. Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).<br /><strong>Windows xp com SP2, Windows xp com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.<br /> | 
| CALG_SHA_384 | 0x0000800d | algoritmo de hash SHA de 384 bits. Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).<br /><strong>Windows xp com SP2, Windows xp com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.<br /> | 
| CALG_SHA_512 | 0x0000800e | algoritmo de hash SHA de 512 bits. Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).<br /><strong>Windows xp com SP2, Windows xp com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.<br /> | 
| CALG_SKIPJACK | 0x0000660a | Skipjack o algoritmo de criptografia de bloco (FORTEZZA). Não há suporte para esse algoritmo. | 
| CALG_SSL2_MASTER | 0x00004c05 | Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 
| CALG_SSL3_MASTER | 0x00004c01 | Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 
| CALG_SSL3_SHAMD5 | 0x00008008 | Usado pelo sistema de operações Schannel.dll. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 
| CALG_TEK | 0x0000660b | TEK (FORTEZZA). Não há suporte para esse algoritmo. | 
| CALG_TLS1_MASTER | 0x00004c06 | Usado pelo sistema de Schannel.dll de operações. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 
| CALG_TLS1PRF | 0x0000800a | Usado pelo sistema de Schannel.dll de operações. Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos. | 




 

Para o Provedor de Criptografia Base da Microsoft, o Provedor Criptográfico Forte da Microsoft e o Provedor criptográfico **aprimorado** da  [Microsoft,](microsoft-strong-cryptographic-provider.md)o ALG_IDs usado para as especificações de chave AT_KEYEXCHANGE e **AT_SIGNATURE** são os exemplos a seguir: [](microsoft-base-cryptographic-provider.md) [](microsoft-enhanced-cryptographic-provider.md)

-   **CALG_RSA_KEYX** é usado para **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** é usado para **AT_SIGNATURE**.

Para o [Microsoft Base DSS](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)e o provedor  criptográfico Diffie-Hellman , os ALG_IDs usados para as especificações de chave **AT_KEYEXCHANGE** e **AT_SIGNATURE** são os exemplos a seguir:

-   **CALG_DH_SF** é usado para **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** é usado para **AT_SIGNATURE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de criptografia](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
