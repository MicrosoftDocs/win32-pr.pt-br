---
description: Remove uma propriedade estendida da coleção.
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: Método ExtendedProperties.Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 684d5abc0a0114e0d2bedb0dc544d50e13337631bb41fb457480dfbe8c5364e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007214"
---
# <a name="extendedpropertiesremove-method"></a>Método ExtendedProperties.Remove

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (Serviços de Invocação de Plataforma) para chamar a função de API Do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O **método Remove** remove uma propriedade estendida da coleção.

## <a name="syntax"></a>Sintaxe


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*propID* \[ Em\]
</dt> <dd>

Um valor da [**enumeração CAPICOM \_ PROPID**](capicom-propid.md) que define os identificadores de propriedade CAPICOM da propriedade estendida a ser removido. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**CAPICOM \_ PROPID \_ UNKNOWN**</dt> </dl>                                                                       | O tipo da propriedade não é conhecido.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ PROV \_ HANDLE**</dt> </dl>                                             | Um handle para um contêiner de chave dentro de um CSP [*(provedor de serviços de*](../secgloss/c-gly.md) criptografia).<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO**</dt> </dl>                                                   | Informações sobre um contêiner de chave em um CSP.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SHA1 \_ HASH**</dt> </dl>                                                                | Um objeto de hash SHA1.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**CAPICOM \_ PROPID \_ HASH \_ PROP**</dt> </dl>                                                                | As propriedades de um objeto hash.<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ MD5 \_ HASH**</dt> </dl>                                                                   | Um objeto de hash MD5.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**CONTEXTO DE CHAVE \_ CAPICOM \_ \_ PROPID**</dt> </dl>                                                          | O contexto [*de chave*](../secgloss/c-gly.md).<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ SPEC**</dt> </dl>                                                                   | As especificações de uma chave.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ IE30 \_ RESERVED**</dt> </dl>                                                    | Informações sobre se o objeto é reservado no Internet Explorer 3.0.<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ PUBKEY \_ HASH \_ RESERVED**</dt> </dl>                              | Informações sobre se o hash da chave pública está reservado.<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**CAPICOM \_ PROPID \_ ENHKEY \_ USAGE**</dt> </dl>                                                       | Um [*EKU (uso de chave) aprimorado.*](../secgloss/e-gly.md)<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**CAPICOM \_ PROPID \_ CTL \_ USAGE**</dt> </dl>                                                                | Um [*uso de*](../secgloss/c-gly.md) CTL (lista de confiança de certificado).<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**CAPICOM \_ PROPID \_ NEXT \_ UPDATE \_ LOCATION**</dt> </dl>                              | O local da próxima atualização para a CRL (lista [*de certificados revogados).*](../secgloss/c-gly.md)<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**CAPICOM \_ PROPID \_ FRIENDLY \_ NAME**</dt> </dl>                                                    | Um nome acessível por humanos.<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**ARQUIVO PVK CAPICOM \_ \_ \_ PROPID**</dt> </dl>                                                                   | Um arquivo que contém uma chave privada.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**CAPICOM \_ PROPID \_ DESCRIPTION**</dt> </dl>                                                           | Uma descrição acessível por humanos.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**ESTADO DE ACESSO \_ PROPID \_ DO CAPICOM \_**</dt> </dl>                                                       | O estado do acesso.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SIGNATURE \_ HASH**</dt> </dl>                                                 | Um hash da assinatura.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**DADOS DE CARTÃO INTELIGENTE \_ CAPICOM \_ \_ \_ PROPID**</dt> </dl>                                             | Dados de cartão inteligente.<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**CAPICOM \_ PROPID \_ EFS**</dt> </dl>                                                                                   | Um Encrypting File System (EFS).<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**CAPICOM \_ PROPID \_ FORTEZZA \_ DATA**</dt> </dl>                                                    | Dados criados usando protocolos criptográficos e algoritmos pertencentes ao NIST (National [*Institute of Standards and Technology).*](../secgloss/n-gly.md)<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**CAPICOM \_ PROPID \_ ARQUIVADO**</dt> </dl>                                                                    | Informações sobre se o objeto está arquivado.<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**IDENTIFICADOR DE \_ CHAVE CAPICOM PROPID \_ \_**</dt> </dl>                                                 | Um identificador de chave.<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**REGISTRO AUTOMÁTICO DO CAPICOM \_ \_ \_ PROPID**</dt> </dl>                                                          | Informações de registro automático para um certificado.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ PARA**</dt> </dl>                                             | Parâmetros para um algoritmo de chave pública.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**CAPICOM \_ PROPID \_ CROSS \_ CERT \_ DIST \_ POINTS**</dt> </dl>                       | Informações usadas para atualizar certificados cruzados dinâmicos.<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ ISSUER \_ PUBLIC \_ KEY \_ MD5 \_ HASH**</dt> </dl>          | O hash MD5 da chave pública do emissor.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SUBJECT \_ PUBLIC \_ KEY \_ MD5 \_ HASH**</dt> </dl>       | O hash MD5 da chave pública do assunto.<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**REGISTRO DO CAPICOM \_ \_ PROPID**</dt> </dl>                                                              | Informações sobre o registro do certificado.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**CAPICOM \_ PROPID \_ DATE \_ STAMP**</dt> </dl>                                                             | Um carimbo de data.<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ ISSUER \_ SERIAL \_ NUMBER \_ MD5 \_ HASH**</dt> </dl> | O hash MD5 do número de série do emissor.<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SUBJECT \_ NAME \_ MD5 \_ HASH**</dt> </dl>                          | O hash MD5 do nome do assunto.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**INFORMAÇÕES DE ERRO ESTENDIDAS DO CAPICOM \_ \_ \_ \_ PROPID**</dt> </dl>                                 | Informações estendidas sobre um erro.<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**RENOVAÇÃO DO CAPICOM \_ \_ PROPID**</dt> </dl>                                                                       | Informações sobre a renovação de uma autoridade [*de certificação*](../secgloss/c-gly.md).<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ ARCHIVED \_ KEY \_ HASH**</dt> </dl>                                       | Um hash arquivado de uma chave.<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ FIRST \_ RESERVED**</dt> </dl>                                                 | Informações sobre a primeira reserva.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ ÚLTIMO \_ RESERVADO**</dt> </dl>                                                    | Informações sobre a reserva mais recente.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**CAPICOM \_ PROPID \_ FIRST \_ USER**</dt> </dl>                                                             | Informações sobre o primeiro usuário.<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**ÚLTIMO USUÁRIO DO CAPICOM \_ \_ \_ PROPID**</dt> </dl>                                                                | Informações sobre o usuário mais recente.<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
