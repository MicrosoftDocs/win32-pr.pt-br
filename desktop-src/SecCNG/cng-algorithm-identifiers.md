---
description: Usado para identificar algoritmos de criptografia padrão em várias funções e estruturas CNG, como a estrutura CRIPTOGRAFAda de \_ interface \_ reg.
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: Identificadores de algoritmo CNG (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f2f9539f9fc446d0c313d32117890bc3b1eff4ed8261a815e41acdda13cbe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908912"
---
# <a name="cng-algorithm-identifiers"></a>Identificadores de algoritmo CNG

Os identificadores a seguir são usados para identificar algoritmos de criptografia padrão em várias funções e estruturas CNG, como a estrutura [**criptografada de \_ interface \_ reg**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) . Provedores de terceiros podem ter algoritmos adicionais para os quais dão suporte.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valor</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt> <dt> &quot; 3DES &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica padrão de criptografia de dados tripla.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt> &quot; 3DES_112 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica padrão de criptografia de dados triplo de 112 bits.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl> <dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt> &quot; AES &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica padrão de criptografia avançada.<br/> Standard: FIPS 197<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt> &quot; AES-CMAC &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica do CMAC (código de autenticação de mensagens baseado em criptografia) com codificação AES.<br/> Standard: SP 800-38B<br/> <strong>Windows 8:</strong> O suporte para este algoritmo começa.<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt> &quot; AES-GMAC &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica GMAC (código de autenticação de mensagem) Galois do padrão de criptografia avançada (AES).<br/> Standard: SP800-38D<br/> <strong>Windows Vista:</strong> esse algoritmo tem suporte a partir do Windows Vista com SP1.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl> <dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt>L &quot; CAPI_KDF &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo da função de derivação da chave da API de criptografia (CAPI). Usado pelas funções <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl> <dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt> &quot; des &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica padrão de criptografia de dados.<br/> Standard: FIPS 46-3, FIPS 81<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl> <dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt> &quot; DESX &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica padrão de criptografia de dados estendidos.<br/> Padrão: nenhum<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl> <dt><strong></strong></dt> <dt> &quot; DH &quot; </dt> BCRYPT_DH_ALGORITHM </dl></td>
<td style="text-align: left;">O algoritmo de troca de chave Diffie-Hellman.<br/> Padrão: #3 PKCS<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt> <dt> &quot; DSA &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de assinatura digital.<br/> Standard: FIPS 186-2<br/> <strong>Windows 8:</strong> a partir do Windows 8, esse algoritmo oferece suporte a FIPS 186-3. Chaves menores ou iguais a 1024 bits aderem ao FIPS 186-2 e às chaves maiores que 1024 a FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt> &quot; ECDH_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">A curva elíptica primo de 256 bits Diffie-Hellman algoritmo de troca de chaves.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt> &quot; ECDH_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">A curva elíptica primo de 384 bits Diffie-Hellman algoritmo de troca de chaves.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt> &quot; ECDH_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">A curva elíptica primo de 521 bits Diffie-Hellman algoritmo de troca de chaves.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de assinatura digital de curva elíptica de 256 bits (FIPS 186-2).<br/> Standard: FIPS 186-2, X 9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de assinatura digital de curva elíptica de 384 bits (FIPS 186-2).<br/> Standard: FIPS 186-2, X 9.62<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de assinatura digital de curva elíptica de 521 bits (FIPS 186-2).<br/> Standard: FIPS 186-2, X 9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl> <dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt> <dt> &quot; MD2 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de hash MD2.<br/> Standard: RFC 1319<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl> <dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt> <dt> &quot; MD4 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de hash MD4.<br/> Standard: RFC 1320<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl> <dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt> <dt> &quot; MD5 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de hash MD5.<br/> Standard: RFC 1321<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl> <dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt> <dt> &quot; RC2 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica do bloqueio RC2.<br/> Standard: RFC 2268<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl> <dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt> &quot; RC4 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica RC4.<br/> Standard: vários<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt> &quot; RNG &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo gerador de número aleatório.<br/> Standard: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br/>
<blockquote>
[!Note]<br />
a partir do Windows Vista com SP1 e Windows Server 2008, o gerador de números aleatórios é baseado no modo de contador AES especificado no padrão NIST SP 800-90.
</blockquote>
<br/> <strong>Windows Vista:</strong> O gerador de número aleatório é baseado no gerador de números aleatórios com base em hash especificado no padrão FIPS 186-2.<br/> <strong>Windows 8:</strong> a partir do Windows 8, o algoritmo RNG dá suporte a FIPS 186-3. Chaves menores ou iguais a 1024 bits aderem ao FIPS 186-2 e às chaves maiores que 1024 a FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt> &quot; DUALECRNG &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo gerador de número aleatório de curva elíptica dupla. <br/> Standard: SP800-90.<br/> <strong>Windows 8:</strong> a partir do Windows 8, o algoritmo EC RNG dá suporte a FIPS 186-3. Chaves menores ou iguais a 1024 bits aderem ao FIPS 186-2 e às chaves maiores que 1024 a FIPS 186-3.<br/> <strong>Windows 10:</strong> a partir do Windows 10, o algoritmo gerador de número aleatório de curva elíptica dupla foi removido. Os usos existentes desse algoritmo continuarão funcionando; no entanto, o gerador de número aleatório é baseado no modo de contador AES especificado no padrão NIST SP 800-90. O novo código deve usar <strong>BCRYPT_RNG_ALGORITHM</strong>, e é recomendável que o código existente seja alterado para usar <strong>BCRYPT_RNG_ALGORITHM</strong>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt> &quot; FIPS186DSARNG &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo gerador de número aleatório adequado para DSA (algoritmo de assinatura digital). <br/> Standard: FIPS 186-2.<br/> <strong>Windows 8:</strong> O suporte para FIPS 186-3 começa.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt> <dt> &quot; RSA &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de chave pública RSA. <br/> Standard: PKCS #1 v 1.5 e v 2.0.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt> &quot; RSA_SIGN &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de assinatura RSA. Atualmente, não há suporte para este algoritmo. Você pode usar o algoritmo <strong>BCRYPT_RSA_ALGORITHM</strong> para executar operações de assinatura RSA. <br/> Standard: PKCS #1 v 1.5 e v 2.0.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl> <dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt> <dt> &quot; SHA1 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de hash seguro de 160 bits. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl> <dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt> <dt> &quot; SHA256 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de hash seguro de 256 bits.<br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl> <dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt> <dt> &quot; Sha384 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de hash seguro de 384 bits. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl> <dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt> <dt> &quot; SHA512 &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de hash seguro de 512 bits. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl> <dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L &quot; SP800_108_CTR_HMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Modo de contador, algoritmo de função de derivação de chave HMAC (código de autenticação de mensagem com base em hash). Usado pelas funções <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl> <dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L &quot; SP800_56A_CONCAT &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo da função de derivação de chave SP800-56A. Usado pelas funções <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl> <dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong> </dt> <dt>L &quot; PBKDF2 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo de função de derivação de chave 2 (PBKDF2) com base em senha. Usado pelas funções <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt> &quot; ECDSA &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo de assinatura digital de curva elíptica de linha genérica (consulte <strong>comentários</strong> para obter mais informações). <br/> Standard: ANSI X 9.62.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt> &quot; ECDH &quot; </dt> </dl></td>
<td style="text-align: left;">Curva elíptica de primo genérica Diffie-Hellman algoritmo de troca de chave (consulte <strong>comentários</strong> para obter mais informações). <br/> Standard: SP800-56A.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl> <dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt> &quot; XTS-AES &quot; </dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia simétrica padrão de criptografia avançada no modo XTS. <br/> Standard: SP-800-38E, IEEE Std 1619-2007.<br/> <strong>Windows 10:</strong> O suporte para este algoritmo começa.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Para usar o algoritmo **BCrypt \_ ECDSA \_ ALGORITM** ou **BCrypt \_ ECDH \_**, chame [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) com algoritmo de ECDSA de **BCrypt \_ \_** ou **\_ \_ algoritmo BCrypt ECDH** como o *pszAlgId*. Em seguida, use [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para definir a propriedade de **nome de \_ \_ curva \_ BCRYPT ECC** para um algoritmo nomeado listado na CNG denominada curvas.

Para os parâmetros de curva elíptica definidos pelo usuário do provedor diretamente, use [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para definir a propriedade de **\_ \_ parâmetros de ECC BCRYPT** . baixe o [Windows 10 CPDK (Kit de desenvolvedor do provedor de criptografia)](https://www.microsoft.com/download/details.aspx?id=30688) para obter mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




