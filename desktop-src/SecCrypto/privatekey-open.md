---
description: Acessa um contêiner de chave existente. Esse método associa o contêiner de chave ao certificado que corresponde à chave privada adicionando a propriedade de ID de props da chave de certificado Prov, que \_ \_ \_ \_ \_ usa as informações especificadas.
ms.assetid: e5e19452-bfdc-4427-ac1d-cf8aa349bb89
title: Método PrivateKey. Open
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7e39738a6e28ebbaffbc867f3098270d5043887a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750750"
---
# <a name="privatekeyopen-method"></a>Método PrivateKey. Open

\[O método **Open** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Open** acessa um contêiner de [*chave*](../secgloss/k-gly.md)existente. Esse método associa o contêiner de chave ao [*certificado*](../secgloss/c-gly.md) que corresponde à [*chave privada*](../secgloss/p-gly.md) adicionando a propriedade de ID de props da chave de certificado Prov, que \_ \_ \_ \_ \_ usa as informações especificadas.

## <a name="syntax"></a>Sintaxe


```VB
PrivateKey.Open( _
  ByVal ContainerName, _
  [ ByVal ProviderName ], _
  [ ByVal ProviderType ], _
  [ ByVal KeySpec ], _
  [ ByVal StoreLocation ], _
  [ ByVal bCheckExistence ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ContainerName* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém o nome do contêiner de chave.

</dd> <dt>

*ProviderName* \[ em, opcional\]
</dt> <dd>

Uma cadeia de caracteres que contém o nome do provedor. O valor padrão é capicore \_ Prov \_ Microsoft \_ Enhanced \_ Prov. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                      | Significado                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_MS_DEF_PROV"></span><span id="capicom_prov_ms_def_prov"></span><dl> <dt>**CAPICOM Prov \_ \_ MS \_ Def \_ Prov**</dt> </dl>                                          | Provedor criptográfico base da Microsoft.<br/>                            |
| <span id="CAPICOM_PROV_MS_ENHANCED_PROV"></span><span id="capicom_prov_ms_enhanced_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ avançado \_ Prov**</dt> </dl>                           | Provedor criptográfico aprimorado da Microsoft.<br/>                        |
| <span id="CAPICOM_PROV_MS_STRONG_PROV"></span><span id="capicom_prov_ms_strong_prov"></span><dl> <dt>**CAPICOM de Prov de \_ \_ segurança da Microsoft \_ \_**</dt> </dl>                                 | Provedor de criptografia forte da Microsoft.<br/>                          |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SIG_PROV"></span><span id="capicom_prov_ms_def_rsa_sig_prov"></span><dl> <dt>**CAPICOM \_ Prov de \_ \_ assinatura RSA de createdef \_ \_ \_ Prov**</dt> </dl>                | Provedor criptográfico da assinatura RSA da Microsoft.<br/>                   |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_rsa_schannel_prov"></span><dl> <dt>**CAPICOM Prov de o \_ \_ \_ \_ RSA \_ Schannel \_ Prov**</dt> </dl> | Provedor criptográfico do Microsoft RSA Schannel.<br/>                    |
| <span id="CAPICOM_PROV_MS_DEF_DSS_PROV"></span><span id="capicom_prov_ms_def_dss_prov"></span><dl> <dt>**CAPICOM o \_ \_ Prov de DSS de MS \_ Def \_ \_**</dt> </dl>                             | Provedor criptográfico Microsoft Base DSS.<br/>                        |
| <span id="CAPICOM_PROV_MS_DEF_DSS_DH_PROV"></span><span id="capicom_prov_ms_def_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Prov de \_ DH do MS \_ Def \_ DSS \_ \_ Prov**</dt> </dl>                   | Microsoft Base DSS e Diffie-Hellman provedor criptográfico.<br/>     |
| <span id="CAPICOM_PROV_MS_ENH_DSS_DH_PROV"></span><span id="capicom_prov_ms_enh_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Prov de \_ \_ ENH \_ DSS \_ DH \_ Prov**</dt> </dl>                   | Microsoft Enhanced DSS e Diffie-Hellman provedor criptográfico.<br/> |
| <span id="CAPICOM_PROV_MS_DEF_DH_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_dh_schannel_prov"></span><dl> <dt>**CAPICOM \_ Prov de \_ \_ \_ DH \_ Schannel \_ do MS def**</dt> </dl>    | Provedor criptográfico Schannel do Microsoft DH.<br/>                     |
| <span id="CAPICOM_PROV_MS_SCARD_PROV"></span><span id="capicom_prov_ms_scard_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ scartar \_ Prov**</dt> </dl>                                    | Provedor criptográfico de cartão inteligente base da Microsoft.<br/>                 |
| <span id="CAPICOM_PROV_MS_ENH_RSA_AES_PROV"></span><span id="capicom_prov_ms_enh_rsa_aes_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ \_ ENH \_ RSA \_ AES \_ Prov**</dt> </dl>                | Provedor criptográfico RSA aprimorado da Microsoft e AES.<br/>            |



 

</dd> <dt>

*ProviderType* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**de \_ \_ tipo CAPICOM Prov**](capicom-prov-type.md) que especifica um tipo de provedor. O valor padrão é capicore \_ Prov \_ RSA \_ Full. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM de \_ \_ RSA Prov \_ Full**</dt> </dl>                 | O CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) completo da [*RSA*](../secgloss/r-gly.md) . Esse tipo de provedor dá suporte a [*assinaturas digitais*](../secgloss/d-gly.md) e [*criptografia*](../secgloss/e-gly.md)de dados.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ SIG**</dt> </dl>                    | O subconjunto do CSP RSA que dá suporte apenas a essas funções e algoritmos necessários para [*hashes*](../secgloss/h-gly.md) e [*assinaturas digitais*](../secgloss/d-gly.md).<br/>                                                                                                                                                                              |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**capicore \_ Prov \_ DSS**</dt> </dl>                                 | O CSP DSS ( [*padrão de assinatura digital*](../secgloss/d-gly.md) ). Esse tipo de provedor dá suporte apenas a hashes e assinaturas digitais. O DSS usa o DSA ( [*algoritmo de assinatura digital*](../secgloss/d-gly.md) ).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**capicor \_ Prov \_ Fortezza**</dt> </dl>                  | O CSP que contém os protocolos criptográficos e os algoritmos de Propriedade do [*Instituto Nacional de normas e tecnologia*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM do \_ \_ Microsoft Prov MS \_ Exchange**</dt> </dl>        | O CSP que dá suporte ao aplicativo de email do Microsoft Exchange e a outros aplicativos que são compatíveis com o Microsoft mail.<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**capicore \_ Prov \_ SSL**</dt> </dl>                                 | O CSP que dá suporte ao protocolo [*protocolo SSL*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**capicore \_ Prov \_ RSA \_ Schannel**</dt> </dl>     | O CSP que dá suporte aos protocolos RSA e [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM de \_ \_ DH Prov DSS \_**</dt> </dl>                       | O CSP que dá suporte aos protocolos DSS e [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**capicore \_ Prov \_ EC \_ ECDSA \_ SIG**</dt> </dl>    | O CSP que dá suporte às funções de ECDSA (algoritmo de assinatura digital de curva elíptica) e algoritmos necessários para assinaturas digitais.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**capicore \_ Prov \_ EC \_ ECNRA \_ SIG**</dt> </dl>    | O CSP que dá suporte à curva elíptica Nyberg-Rueppel funções analógicas (ECNRA) e algoritmos necessários para assinaturas digitais.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM de ECDSA do EC para o \_ \_ \_ \_ completo**</dt> </dl> | O CSP que dá suporte ao ECDSA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**capicore \_ Prov \_ EC \_ ECNRA \_ Full**</dt> </dl> | O CSP que dá suporte ao ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**capicore \_ Prov \_ DH \_ Schannel**</dt> </dl>        | O CSP que dá suporte aos protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) e [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ SPYRUS \_ Lynks**</dt> </dl>     | O CSP que dá suporte ao dispositivo de cartão SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ Prov \_ RNG**</dt> </dl>                                 | O CSP que lida com a geração de números aleatórios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM de \_ Prov \_ Intel \_ SEC**</dt> </dl>              | O CSP que fornece segurança Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ Prov \_ substituir \_ OWF**</dt> </dl>        | O CSP que dá suporte à substituição da maneira em que os formatos unidirecionais são gerados a partir de senhas.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM do \_ \_ \_ AES RSA**</dt> </dl>                    | O CSP que dá suporte a assinaturas digitais e criptografia de dados usando o algoritmo criptografia AES ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

*KeySpec* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**de \_ \_ espec de chave de CAPICOM**](capicom-key-spec.md) que especifica o tipo de chave privada. O valor padrão é capicote \_ Key \_ spec \_ Signature. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                        | Significado                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**chave de capicor \_ \_ spec Key \_ Exchange**</dt> </dl> | A chave pode ser usada para criptografia e assinatura.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**\_assinatura de \_ espec de chave de CAPICOM \_**</dt> </dl>       | A chave só pode ser usada para assinatura.<br/>           |



 

</dd> <dt>

*StoreLocation* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**do \_ \_ local de armazenamento capicor**](capicom-store-location.md) que especifica o local do repositório onde a chave reside. O valor padrão é capicote \_ \_ user \_ Store atual. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_armazenamento de memória CApicom \_**</dt> </dl>                                                | O repositório é um repositório de memória. As alterações no conteúdo da loja não são persistentes.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**CAPICOM do \_ \_ armazenamento do computador local \_**</dt> </dl>                          | O repositório é um repositório do computador local. As lojas de computadores locais poderão ser armazenamentos de leitura/gravação somente se o usuário tiver permissões de leitura/gravação. Se o usuário tiver permissões de leitura/gravação e se o repositório for aberto como leitura/gravação, as alterações no conteúdo do repositório serão persistidas.<br/> |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**\_armazenamento de \_ usuário \_ atual do CAPICOM**</dt> </dl>                             | O repositório é um armazenamento de usuário atual. Um armazenamento de usuário atual pode ser um repositório de leitura/gravação. Se for, as alterações no conteúdo do repositório serão persistidas.<br/>                                                                                                                        |
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**armazenamento de usuários do CAPICOM \_ \_ do Active Directory \_ \_**</dt> </dl> | O repositório é um repositório Active Directory. Active Directory armazenamentos só podem ser abertos no modo somente leitura. Os certificados não podem ser adicionados ou removidos de repositórios Active Directory.<br/>                                                                                          |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**\_armazenamento de \_ usuário do cartão inteligente \_ CAPICOM \_**</dt> </dl>                   | O repositório é o grupo de cartões inteligentes presentes. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*bCheckExistence* \[ em, opcional\]
</dt> <dd>

Um valor booliano que indica se o capicor tentará acessar a chave. Se **for true**, o capicor tentará acessar a chave. Se a chave for protegida pelo usuário ou em um cartão inteligente ou outro dispositivo, uma caixa de diálogo poderá ser gerada. O valor padrão é **Falso**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método retorna CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> <dt>

[**Certificate. HasPrivateKey**](certificate-hasprivatekey.md)
</dt> </dl>

 

 
