---
description: Recupera um valor da enumeração do tipo CAPICOM \_ Prov \_ que especifica o tipo de provedor.
ms.assetid: bc6a579f-5532-45e3-97f4-adcde2cd29e5
title: Propriedade PrivateKey. ProviderType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderType
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b38cc9a030bc27a30a66624f1faeca080104e7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778674"
---
# <a name="privatekeyprovidertype-property"></a>Propriedade PrivateKey. ProviderType

\[A propriedade **ProviderType** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **ProviderType** recupera um valor da enumeração [**de \_ \_ tipo CAPICOM Prov**](capicom-prov-type.md) que especifica o tipo de provedor.

## <a name="syntax"></a>Sintaxe


```VB
PrivateKey.ProviderType As CAPICOM_PROV_TYPE
```



## <a name="property-value"></a>Valor da propriedade

Um valor da enumeração [**de \_ \_ tipo CAPICOM Prov**](capicom-prov-type.md) que indica o tipo de provedor. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM de \_ \_ RSA Prov \_ Full**</dt> </dl>                 | O CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) completo da [*RSA*](../secgloss/r-gly.md) . Esse tipo de provedor dá suporte a [*assinaturas digitais*](../secgloss/d-gly.md) e [*criptografia*](../secgloss/e-gly.md)de dados.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ SIG**</dt> </dl>                    | O subconjunto do CSP RSA que dá suporte apenas a funções e algoritmos necessários para hashes e assinaturas digitais.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**capicore \_ Prov \_ DSS**</dt> </dl>                                 | O CSP DSS ( [*padrão de assinatura digital*](../secgloss/d-gly.md) ). Esse tipo de provedor dá suporte apenas a hashes e assinaturas digitais. O DSS usa o DSA ( [*algoritmo de assinatura digital*](../secgloss/d-gly.md) ).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**capicor \_ Prov \_ Fortezza**</dt> </dl>                  | O CSP que contém os protocolos criptográficos e os algoritmos de Propriedade do [*Instituto Nacional de normas e tecnologia*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM do \_ \_ Microsoft Prov MS \_ Exchange**</dt> </dl>        | O CSP projetado para as necessidades criptográficas do aplicativo de email do Microsoft Exchange e de outros aplicativos compatíveis com o Microsoft mail.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**capicore \_ Prov \_ SSL**</dt> </dl>                                 | O CSP que dá suporte ao protocolo [*protocolo SSL*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**capicore \_ Prov \_ RSA \_ Schannel**</dt> </dl>     | O CSP que dá suporte aos protocolos RSA e [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM de \_ \_ DH Prov DSS \_**</dt> </dl>                       | O CSP que dá suporte aos protocolos de [*padrão de assinatura digital*](../secgloss/d-gly.md) (DSS) e [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                           |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**capicore \_ Prov \_ EC \_ ECDSA \_ SIG**</dt> </dl>    | O CSP que dá suporte às funções de ECDSA (algoritmo de assinatura digital de curva elíptica) e algoritmos necessários para assinaturas digitais.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**capicore \_ Prov \_ EC \_ ECNRA \_ SIG**</dt> </dl>    | O CSP que dá suporte à curva elíptica Nyberg-Rueppel funções analógicas (ECNRA) e algoritmos necessários para assinaturas digitais.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM de ECDSA do EC para o \_ \_ \_ \_ completo**</dt> </dl> | O CSP que dá suporte ao ECDSA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**capicore \_ Prov \_ EC \_ ECNRA \_ Full**</dt> </dl> | O CSP que dá suporte ao ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**capicore \_ Prov \_ DH \_ Schannel**</dt> </dl>        | O CSP que dá suporte aos protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) e [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ SPYRUS \_ Lynks**</dt> </dl>     | O CSP que dá suporte ao dispositivo de cartão SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ Prov \_ RNG**</dt> </dl>                                 | O CSP que lida com a geração de números aleatórios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM de \_ Prov \_ Intel \_ SEC**</dt> </dl>              | O CSP que fornece segurança Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ Prov \_ substituir \_ OWF**</dt> </dl>        | O CSP que dá suporte à substituição da maneira em que os formatos unidirecionais (OWFs) são gerados a partir de senhas.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM do \_ \_ \_ AES RSA**</dt> </dl>                    | O CSP que dá suporte a assinaturas digitais e criptografia de dados usando o algoritmo [*criptografia AES*](../secgloss/a-gly.md) (AES).<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
