---
description: Recupera informações do certificado.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'Método ICertificate2:: GetInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 401aa077e5f736449e0638fd5cf368224485ec8393b8bddaed1f62296ad90297
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127016"
---
# <a name="icertificate2getinfo-method"></a>Método ICertificate2:: GetInfo

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **GetInfo** recupera informações do [*certificado*](../secgloss/c-gly.md).

## <a name="syntax"></a>Sintaxe


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InfoType* \[ no\]
</dt> <dd>

Um valor da enumeração [**de \_ \_ \_ tipo de informações do certificado capicor**](capicom-cert-info-type.md) que especifica que tipo de dados é recuperado do certificado. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**informações de certificado capicor \_ \_ \_ \_ nome simples da entidade \_**</dt> </dl> | Retorna o nome de exibição da entidade do certificado.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**\_ \_ \_ nome simples do emissor de informações de \_ certificado CAPICOM \_**</dt> </dl>    | Retorna o nome de exibição do emissor do certificado.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**CAPICOM \_ informações de certificado \_ nome de \_ email da entidade \_ \_**</dt> </dl>    | Retorna o endereço de email da entidade do certificado.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**capicor \_ informações do certificado \_ nome do \_ email do emissor \_ \_**</dt> </dl>       | Retorna o endereço de email do emissor do certificado.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**informações de certificado capicor \_ \_ \_ UPN da entidade \_**</dt> </dl>                          | Retorna o UPN da entidade do certificado. Introduzido no CAPICOM 2,0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**\_UPN do \_ emissor de informações de certificado CAPICOM \_ \_**</dt> </dl>                             | Retorna o UPN do emissor do certificado. Introduzido no CAPICOM 2,0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**CAPICOM \_ informações do certificado \_ \_ \_ nome DNS da entidade \_**</dt> </dl>          | Retorna o nome DNS da entidade do certificado. Introduzido no CAPICOM 2,0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**CAPICOM \_ informações do certificado \_ \_ \_ nome DNS do emissor \_**</dt> </dl>             | Retorna o nome DNS do emissor do certificado. Introduzido no CAPICOM 2,0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma cadeia de caracteres que contém as informações solicitadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
