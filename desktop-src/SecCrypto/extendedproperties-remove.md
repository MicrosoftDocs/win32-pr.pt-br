---
description: Remove uma propriedade estendida da coleção.
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: Método ExtendedProperties. Remove
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
ms.openlocfilehash: 1774ce0fc8b03bed621c58b0f7a9a0f16a7d4156
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778687"
---
# <a name="extendedpropertiesremove-method"></a>Método ExtendedProperties. Remove

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O método **Remove** remove uma propriedade estendida da coleção.

## <a name="syntax"></a>Sintaxe


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*propID* \[ no\]
</dt> <dd>

Um valor da enumeração [**\_ Propid de CAPICOM**](capicom-propid.md) que define os identificadores de propriedade CAPICOM da propriedade estendida a ser removida. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**capico de \_ Propid \_ desconhecido**</dt> </dl>                                                                       | O tipo da propriedade não é conhecido.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**\_identificador de \_ Prov de chave Propid \_ de CAPICOM \_**</dt> </dl>                                             | Um identificador para um contêiner de chave em um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**\_informações de \_ Prov de chave Propid \_ de CAPICOM \_**</dt> </dl>                                                   | Informações sobre um contêiner de chave em um CSP.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**\_ \_ Hash SHA1 de CAPICOM Propid \_**</dt> </dl>                                                                | Um objeto hash SHA1.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**PROP. de \_ hash Propid de CApicom \_ \_**</dt> </dl>                                                                | As propriedades de um objeto de hash.<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**\_ \_ Hash MD5 de CAPICOM de Propid \_**</dt> </dl>                                                                   | Um objeto hash MD5.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**\_contexto de \_ chave de Propid de CAPICOM \_**</dt> </dl>                                                          | O [*contexto*](../secgloss/c-gly.md)de chave.<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**\_especificação de \_ chave de Propid de CAPICOM \_**</dt> </dl>                                                                   | As especificações de uma chave.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**Capicor \_ Propid \_ IE30 \_ reservado**</dt> </dl>                                                    | Informações sobre se o objeto está reservado no Internet Explorer 3,0.<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**HASH de capicot \_ Propid \_ PUBKEY \_ \_ reservado**</dt> </dl>                              | Informações sobre se o hash da chave pública está reservado.<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**uso de CAPICOM de \_ utilização de Propid \_ \_**</dt> </dl>                                                       | Um EKU ( [*uso avançado de chave*](../secgloss/e-gly.md) ).<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**uso da CTL de CAPICOM \_ Propid \_ \_**</dt> </dl>                                                                | Um uso de CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ).<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**\_ \_ próximo local de \_ atualização \_ do CAPICOM propid**</dt> </dl>                              | O local da próxima atualização para a CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ).<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**\_ \_ nome amigável do CAPICOM de Propid \_**</dt> </dl>                                                    | Um nome legível.<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**arquivo do capico de \_ Propid \_ PVK \_**</dt> </dl>                                                                   | Um arquivo que contém uma chave privada.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**Descrição do CAPICOM \_ Propid \_**</dt> </dl>                                                           | Uma descrição legível.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**Estado de acesso do CAPICOM \_ Propid \_ \_**</dt> </dl>                                                       | O estado do acesso.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**\_hash de \_ assinatura \_ Propid CAPICOM**</dt> </dl>                                                 | Um hash da assinatura.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**\_dados de \_ \_ cartão inteligente \_ CAPICOM de propid**</dt> </dl>                                             | Dados do cartão inteligente.<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**CAPICOM do \_ \_ EFS propid**</dt> </dl>                                                                                   | Um sistema de arquivos com criptografia (EFS).<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**dados do CAPICOM de \_ Fortezza de Propid \_ \_**</dt> </dl>                                                    | Dados criados usando os protocolos criptográficos e algoritmos de Propriedade do [*Instituto Nacional de normas e tecnologia*](../secgloss/n-gly.md) (NIST).<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**CAPICOM \_ \_ arquivo morto de propid**</dt> </dl>                                                                    | Informações sobre se o objeto é arquivado.<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**\_identificador de \_ chave de Propid de CAPICOM \_**</dt> </dl>                                                 | Um identificador de chave.<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**\_ \_ registro automático de Propid de CAPICOM \_**</dt> </dl>                                                          | Informações de registro automático para um certificado.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**CAPICOM \_ Propid \_ PUBKEY \_ alg \_ para**</dt> </dl>                                             | Parâmetros para um algoritmo de chave pública.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**\_pontos de \_ distribuição de certificado cruzado Propid de \_ \_ CAPICOM \_**</dt> </dl>                       | Informações usadas para atualizar certificados cruzados dinâmicos.<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**\_ \_ \_ \_ Hash MD5 de chave pública \_ do emissor de Propid \_ de CAPICOM**</dt> </dl>          | O hash MD5 da chave pública do emissor.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**\_ \_ \_ \_ Hash MD5 da chave pública \_ \_ do CAPICOM de requerente propid**</dt> </dl>       | O hash MD5 da chave pública da entidade.<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**registro do CAPICOM de \_ Propid \_**</dt> </dl>                                                              | Informações sobre o registro do certificado.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**\_carimbo de \_ data de Propid de CAPICOM \_**</dt> </dl>                                                             | Um carimbo de data/hora.<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**\_ \_ \_ \_ Hash MD5 de número de série \_ do \_ emissor propid do CAPICOM**</dt> </dl> | O hash MD5 do número de série do emissor.<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**\_ \_ \_ Hash MD5 de nome de entidade \_ do \_ CAPICOM**</dt> </dl>                          | O hash MD5 do nome da entidade.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**\_informações de \_ erro estendido Propid \_ de CAPICOM \_**</dt> </dl>                                 | Informações estendidas sobre um erro.<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**\_renovação de Propid de CApicom \_**</dt> </dl>                                                                       | Informações sobre a renovação de uma [*autoridade de certificação*](../secgloss/c-gly.md).<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**\_hash de \_ chave arquivada Propid \_ CAPICOM \_**</dt> </dl>                                       | Um hash arquivado de uma chave.<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**capicor \_ Propid \_ primeiro \_ reservado**</dt> </dl>                                                 | Informações sobre a primeira reserva.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**capicor \_ Propid \_ por último \_ reservado**</dt> </dl>                                                    | Informações sobre a reserva mais recente.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**capicore \_ Propid \_ First \_ User**</dt> </dl>                                                             | Informações sobre o primeiro usuário.<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**CAPICOM \_ propid do \_ último \_ usuário**</dt> </dl>                                                                | Informações sobre o usuário mais recente.<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
