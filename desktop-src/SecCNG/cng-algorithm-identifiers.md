---
description: Usado para identificar algoritmos de criptografia padrão em várias funções e estruturas CNG, como a estrutura \_ REG da INTERFACE \_ CRYPT.
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: Identificadores de algoritmo CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e853d7cd0d1dd34104d3cffa20f301c11e45304c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481882"
---
# <a name="cng-algorithm-identifiers"></a>Identificadores de algoritmo CNG

Os identificadores a seguir são usados para identificar algoritmos de criptografia padrão em várias funções e estruturas CNG, como a estrutura [**\_ REG da INTERFACE \_ CRYPT.**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) Provedores de terceiros podem ter algoritmos adicionais que eles suportam.




| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl><dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt><dt>"3DES"</dt></dl> | O algoritmo de criptografia simétrica padrão de criptografia de dados triplo.<br /> Padrão: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl><dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt><dt>"3DES_112"</dt></dl> | O algoritmo de criptografia simétrica padrão de criptografia de dados triplos de 112 bits.<br /> Padrão: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl><dt><strong>BCRYPT_AES_ALGORITHM</strong></dt><dt>"AES"</dt></dl> | O algoritmo de criptografia simétrica padrão de criptografia avançada.<br /> Padrão: FIPS 197<br /> | 
| <span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt><dt>"AES-CMAC"</dt></dl> | O algoritmo de criptografia simétrica CMAC (código de autenticação de mensagem baseado em criptografia AES) avançado.<br /> Padrão: SP 800-38B<br /><strong>Windows 8:</strong> O suporte para esse algoritmo começa.<br /><br /> | 
| <span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt><dt>"AES-GMAC"</dt></dl> | O algoritmo de criptografia simétrica GMAC (código de autenticação de mensagem) AES (padrão de criptografia avançada).<br /> Padrão: SP800-38D<br /><strong>Windows Vista:</strong> Esse algoritmo tem suporte a partir do Windows Vista com SP1.<br /> | 
| <span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl><dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt><dt>L"CAPI_KDF"</dt></dl> | Algoritmo de função de derivação de chave CAPI (API de Criptografia). Usado pelas <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funções BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br /> | 
| <span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl><dt><strong>BCRYPT_DES_ALGORITHM</strong></dt><dt>"DES"</dt></dl> | O algoritmo de criptografia simétrica padrão de criptografia de dados.<br /> Padrão: FIPS 46-3, FIPS 81<br /> | 
| <span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl><dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt><dt>"DESX"</dt></dl> | O algoritmo de criptografia simétrica padrão de criptografia de dados estendido.<br /> Padrão: Nenhum<br /> | 
| <span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl><dt><strong>BCRYPT_DH_ALGORITHM</strong></dt><dt>"DH"</dt></dl> | O Diffie-Hellman de troca de chaves.<br /> Padrão: PKCS #3<br /> | 
| <span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl><dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt><dt>"DSA"</dt></dl> | O algoritmo de assinatura digital.<br /> Padrão: FIPS 186-2<br /><strong>Windows 8:</strong> Começando com Windows 8, esse algoritmo dá suporte a FIPS 186-3. Chaves menores ou iguais a 1024 bits aderem a FIPS 186-2 e chaves maiores que 1024 a FIPS 186-3.<br /> | 
| <span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt><dt>"ECDH_P256"</dt></dl> | A curva elíptica principal de 256 bits Diffie-Hellman algoritmo de troca de chaves.<br /> Padrão: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt><dt>"ECDH_P384"</dt></dl> | A curva elíptica principal de 384 bits Diffie-Hellman algoritmo de troca de chaves.<br /> Padrão: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt><dt>"ECDH_P521"</dt></dl> | A curva elíptica principal de 521 bits Diffie-Hellman algoritmo de troca de chaves.<br /> Padrão: SP800-56A<br /> | 
| <span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt><dt>"ECDSA_P256"</dt></dl> | O algoritmo de assinatura digital de curva elíptica principal de 256 bits (FIPS 186-2).<br /> Padrão: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt><dt>"ECDSA_P384"</dt></dl> | O algoritmo de assinatura digital de curva elíptica principal de 384 bits (FIPS 186-2).<br /> Padrão: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt><dt>"ECDSA_P521"</dt></dl> | O algoritmo de assinatura digital de curva elíptica principal de 521 bits (FIPS 186-2).<br /> Padrão: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl><dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt><dt>"MD2"</dt></dl> | O algoritmo de hash MD2.<br /> Padrão: RFC 1319<br /> | 
| <span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl><dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt><dt>"MD4"</dt></dl> | O algoritmo de hash MD4.<br /> Padrão: RFC 1320<br /> | 
| <span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl><dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt><dt>"MD5"</dt></dl> | O algoritmo de hash MD5.<br /> Padrão: RFC 1321<br /> | 
| <span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl><dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt><dt>"RC2"</dt></dl> | O algoritmo de criptografia simétrica de bloco RC2.<br /> Padrão: RFC 2268<br /> | 
| <span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl><dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt><dt>"RC4"</dt></dl> | O algoritmo de criptografia simétrica RC4.<br /> Padrão: vários<br /> | 
| <span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl><dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt><dt>"RNG"</dt></dl> | O algoritmo gerador de número aleatório.<br /> Padrão: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br /><blockquote>[!Note]<br />A partir do Windows Vista com SP1 e Windows Server 2008, o gerador de número aleatório é baseado no modo de contador AES especificado no padrão NIST SP 800-90.</blockquote><br /><strong>Windows Vista:</strong> O gerador de número aleatório baseia-se no gerador de número aleatório baseado em hash especificado no padrão FIPS 186-2.<br /><strong>Windows 8:</strong> Começando com Windows 8, o algoritmo RNG dá suporte a FIPS 186-3. Chaves menores ou iguais a 1024 bits aderem a FIPS 186-2 e chaves maiores que 1024 a FIPS 186-3.<br /> | 
| <span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl><dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt><dt>"DUALECRNG"</dt></dl> | O algoritmo gerador de número aleatório de curva elíptica dupla. <br /> Padrão: SP800-90.<br /><strong>Windows 8:</strong> Começando com Windows 8, o algoritmo EC RNG dá suporte a FIPS 186-3. Chaves menores ou iguais a 1024 bits aderem a FIPS 186-2 e chaves maiores que 1024 a FIPS 186-3.<br /><strong>Windows 10:</strong> Começando com Windows 10, o algoritmo gerador de número aleatório de curva elíptica dupla foi removido. Os usos existentes desse algoritmo continuarão a funcionar; no entanto, o gerador de número aleatório baseia-se no modo de contador AES especificado no padrão NIST SP 800-90. O novo código deve <strong>usar BCRYPT_RNG_ALGORITHM</strong>e é recomendável que o código existente seja alterado para usar <strong>BCRYPT_RNG_ALGORITHM</strong>. <br /> | 
| <span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl><dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt><dt>"FIPS186DSARNG"</dt></dl> | O algoritmo gerador de número aleatório adequado para DSA (Algoritmo de Assinatura Digital). <br /> Padrão: FIPS 186-2.<br /><strong>Windows 8:</strong> O suporte para FIPS 186-3 começa.<br /> | 
| <span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl><dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt><dt>"RSA"</dt></dl> | O algoritmo de chave pública RSA. <br /> Padrão: PKCS #1 v1.5 e v2.0.<br /> | 
| <span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl><dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt><dt>"RSA_SIGN"</dt></dl> | O algoritmo de assinatura RSA. Atualmente, não há suporte para esse algoritmo. Você pode usar o algoritmo <strong>BCRYPT_RSA_ALGORITHM</strong> para executar operações de assinatura RSA. <br /> Standard: PKCS #1 v 1.5 e v 2.0.<br /> | 
| <span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl><dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt><dt>"SHA1"</dt></dl> | O algoritmo de hash seguro de 160 bits. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl><dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt><dt>"SHA256"</dt></dl> | O algoritmo de hash seguro de 256 bits.<br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl><dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt><dt>"Sha384"</dt></dl> | O algoritmo de hash seguro de 384 bits. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl><dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt><dt>"sha512"</dt></dl> | O algoritmo de hash seguro de 512 bits. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl><dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt><dt>L "SP800_108_CTR_HMAC"</dt></dl> | Modo de contador, algoritmo de função de derivação de chave HMAC (código de autenticação de mensagem com base em hash). Usado pelas funções <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br /> | 
| <span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl><dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt><dt>L "SP800_56A_CONCAT"</dt></dl> | Algoritmo da função de derivação de chave SP800-56A. Usado pelas funções <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br /> | 
| <span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl><dt><strong>BCRYPT_PBKDF2_ALGORITHM</strong></dt><dt>L "PBKDF2"</dt></dl> | Algoritmo de função de derivação de chave 2 (PBKDF2) com base em senha. Usado pelas funções <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br /> | 
| <span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt><dt>"ECDSA"</dt></dl> | Algoritmo de assinatura digital de curva elíptica de linha genérica (consulte <strong>comentários</strong> para obter mais informações). <br /> Standard: ANSI X 9.62.<br /> | 
| <span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt><dt>"ECDH"</dt></dl> | Curva elíptica de primo genérica Diffie-Hellman algoritmo de troca de chave (consulte <strong>comentários</strong> para obter mais informações). <br /> Standard: SP800-56A.<br /> | 
| <span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl><dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt><dt>"XTS-AES"</dt></dl> | O algoritmo de criptografia simétrica padrão de criptografia avançada no modo XTS. <br /> Standard: SP-800-38E, IEEE Std 1619-2007.<br /><strong>Windows 10:</strong> O suporte para este algoritmo começa.<br /> | 




## <a name="remarks"></a>Comentários

Para usar o algoritmo **BCrypt \_ ECDSA \_ ALGORITM** ou **BCrypt \_ ECDH \_**, chame [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) com algoritmo de ECDSA de **BCrypt \_ \_** ou **\_ \_ algoritmo BCrypt ECDH** como o *pszAlgId*. Em seguida, use [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para definir a propriedade de **nome de \_ \_ curva \_ BCRYPT ECC** para um algoritmo nomeado listado na CNG denominada curvas.

Para os parâmetros de curva elíptica definidos pelo usuário do provedor diretamente, use [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para definir a propriedade de **\_ \_ parâmetros de ECC BCRYPT** . baixe o [Windows 10 CPDK (Kit de desenvolvedor do provedor de criptografia)](https://www.microsoft.com/download/details.aspx?id=30688) para obter mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




