---
description: Retorna um objeto Certificates que contém todos os certificados que correspondem aos critérios de pesquisa especificados.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: 'Método ICertificates2:: find'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Find
- ICertificates2.Find
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9ea15891c33a0789e5b6746b55dfd0b0eb602afc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752339"
---
# <a name="icertificates2find-method"></a>Método ICertificates2:: find

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Find** retorna um objeto de [**certificados**](certificates.md) que contém todos os certificados que correspondem aos critérios de pesquisa especificados. Esse método foi introduzido no CAPICOM 2,0.

## <a name="syntax"></a>Sintaxe


```VB
Certificates.Find( _
  ByVal FindType, _
  [ ByVal varCriteria ], _
  [ ByVal bFindValidOnly ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localizar* \[ no\]
</dt> <dd>

Um valor da enumeração [**de \_ \_ \_ tipo de certificado capicor**](capicom-certificate-find-type.md) que especifica o tipo de critério de correspondência fornecido no parâmetro *varCriteria* . A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**Certificado capicor \_ \_ localizar \_ \_ hash SHA1**</dt> </dl>                              | Retorna certificados com um hash SHA1 que corresponde ao hash SHA1 especificado no parâmetro *varCriteria* .<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**certificado CAPICOM \_ \_ localizar \_ nome da entidade \_**</dt> </dl>                     | Retorna certificados cujo nome da entidade corresponde exatamente ou parcialmente ao nome da entidade especificada no parâmetro *varCriteria* . Essa chamada pesquisa apenas o campo nome da entidade.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**\_nome do \_ emissor da localização do certificado CAPICOM \_ \_**</dt> </dl>                        | Retorna certificados cujo nome do emissor corresponde exatamente ou parcialmente ao nome do emissor especificado no parâmetro *varCriteria* . Essa chamada pesquisa apenas o campo nome do emissor.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**\_nome da \_ raiz de localização do certificado CAPICOM \_ \_**</dt> </dl>                              | Retorna certificados cujo nome da entidade raiz corresponde exatamente ou parcialmente ao nome da entidade raiz especificado no parâmetro *varCriteria* . Essa chamada cria uma cadeia. Essa chamada pesquisa o campo nome da entidade do certificado raiz.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**\_nome do \_ modelo de localização do certificado CAPICOM \_ \_**</dt> </dl>                  | Retorna certificados cujo nome de modelo corresponde ao nome de modelo especificado no parâmetro *varCriteria* .<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**\_extensão de \_ localização de certificado CAPICOM \_**</dt> </dl>                               | Retorna certificados que têm uma extensão que corresponde à extensão especificada no parâmetro *varCriteria* .<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**certificado capicor \_ \_ localizar \_ propriedade estendida \_**</dt> </dl>      | Retorna certificados no repositório que contêm explicitamente uma propriedade estendida com o valor especificado no parâmetro *varCriteria* .<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**certificado CAPICOM ao \_ \_ localizar \_ política de aplicativo \_**</dt> </dl>   | Retorna certificados no repositório que têm uma extensão de uso avançado de chave, extensão de política de aplicativo ou propriedade estendida especificada no parâmetro *varCriteria* .<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**\_política de \_ certificado de localização de certificado CAPICOM \_ \_**</dt> </dl>   | Retorna certificados que contêm o OID da política na extensão de política de certificado especificada no parâmetro *varCriteria* .<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**tempo de localização de certificado capicor \_ \_ \_ \_ válido**</dt> </dl>                           | Retorna certificados cujo tempo é válido.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**tempo de localização de certificado capico \_ \_ \_ \_ \_ ainda não \_ válido**</dt> </dl> | Retorna certificados cujo tempo ainda não é válido.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**tempo limite de localização do certificado CAPICOM \_ \_ \_ \_ expirado**</dt> </dl>                     | Retorna certificados cujo tempo expirou.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**\_uso da \_ chave de localização de certificado CAPICOM \_ \_**</dt> </dl>                              | Retorna certificados que contêm usos de chave na extensão KeyUsage especificada no parâmetro *varCriteria* . Se a extensão KeyUsage não estiver presente, todos os usos da chave serão considerados indisponíveis.<br/>                           |



 

</dd> <dt>

*varCriteria* \[ em, opcional\]
</dt> <dd>

Uma variante que contém os critérios de pesquisa. Esses dados devem corresponder ao tipo de dados especificado no parâmetro *FindType* . Se o valor do parâmetro *FindType* for CAPICOM \_ \_ tempo de localização de certificado \_ \_ válido, o tempo de espera de localização do \_ certificado \_ \_ \_ ainda não for \_ \_ válido ou \_ \_ \_ \_ o tempo de falha da localização do certificado causador expirar e você não passar um valor para esse parâmetro, a hora atual será assumida. Para obter exemplos de cada tipo de dados, consulte comentários. O valor padrão é 0.

</dd> <dt>

*bFindValidOnly* \[ em, opcional\]
</dt> <dd>

Um valor booliano que indica se apenas certificados válidos são retornados. O valor padrão é false; Isso indica que todos os certificados que correspondem aos critérios de pesquisa são retornados.

Se for true, a pesquisa não retornará os seguintes tipos de certificados:

-   Certificados cujo tempo expirou ou ainda não é válido.
-   Certificados não encadeados corretamente.
-   Certificados que têm problemas de assinatura.
-   Certificados que são revogados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Objeto de [**certificados**](certificates.md) que contém os resultados da pesquisa.

**Capicom 2,1:** O objeto [**Certificates**](certificates.md) retornado contém referências aos certificados na coleção em que a pesquisa foi feita. Todas as alterações feitas nos certificados no objeto de **certificados** retornados são refletidas nessa coleção.

**Capicom 2,0, CApicom 2.0.0.1, CApicom 2.0.0.2 e CApicom 2.0.0.3:** O objeto de [**certificados**](certificates.md) que é retornado contém cópias dos certificados na coleção em que a pesquisa foi feita. As alterações feitas nos certificados no objeto de **certificados** retornados não são refletidas nessa coleção.

## <a name="remarks"></a>Comentários

Os exemplos a seguir mostram possíveis critérios de pesquisa para os diferentes tipos de critérios de pesquisa.



| Parâmetro *FindType*                              | parâmetro *varCriteria*                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Certificado capicor \_ \_ localizar \_ \_ hash SHA1            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| certificado CAPICOM \_ \_ localizar \_ nome da entidade \_         | "NameOfPerson"                                                                                                                     |
| \_nome do \_ emissor da localização do certificado CAPICOM \_ \_          | VeriSign                                                                                                                         |
| \_nome da \_ raiz de localização do certificado CAPICOM \_ \_            | "Autoridade raiz da Microsoft"                                                                                                         |
| \_nome do \_ modelo de localização do certificado CAPICOM \_ \_        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| \_extensão de \_ localização de certificado CAPICOM \_             | "2.5.29.31"<br/> \_extensão de \_ uso da chave \_ \_ capicor OID<br/> "Lista de distribuição de CRL"<br/>                           |
| certificado capicor \_ \_ localizar \_ propriedade estendida \_    | \_informações de \_ Prov de chave Propid \_ de CAPICOM \_                                                                                                   |
| certificado CAPICOM ao \_ \_ localizar \_ política de aplicativo \_   | "1.3.6.1.5.5.7.3.3"<br/> 1.3.6.1.5.5.7.3.4<br/> \_EKU de \_ autenticação de servidor \_ \_ capicor OID<br/> "Assinatura de código"<br/> |
| \_política de \_ certificado de localização de certificado CAPICOM \_ \_   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Alta garantia corporativa"<br/>                                                           |
| tempo de localização de certificado capicor \_ \_ \_ \_ válido           | \#04/15/2002, 6:00 PM\#                                                                                                            |
| tempo de localização de certificado capico \_ \_ \_ \_ \_ ainda não \_ válido | \#04/15/2002, 6:00 PM\#                                                                                                            |
| tempo limite de localização do certificado CAPICOM \_ \_ \_ \_ expirado         | \#04/15/2002, 6:00 PM\#                                                                                                            |
| \_uso da \_ chave de localização de certificado CAPICOM \_ \_            | somente criptografia de capicos de \_ \_ \_ uso de chave \_                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificados**](certificates.md)
</dt> <dt>

[**OID de CAPICOM \_**](capicom-oid.md)
</dt> </dl>

 

 
