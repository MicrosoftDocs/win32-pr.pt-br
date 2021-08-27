---
description: Retorna um objeto Certificates que contém todos os certificados que corresponderem aos critérios de pesquisa especificados.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: Método ICertificates2::Find
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
ms.openlocfilehash: 51e3d19348f0bff9cdbe0b4211d648a25025b2a3ab8feee9df6f804486265857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100986"
---
# <a name="icertificates2find-method"></a>Método ICertificates2::Find

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método Find** retorna um objeto [**Certificates**](certificates.md) que contém todos os certificados que corresponderem aos critérios de pesquisa especificados. Esse método foi introduzido no CAPICOM 2.0.

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

*FindType* \[ Em\]
</dt> <dd>

Um valor da [**enumeração CAPICOM \_ CERTIFICATE FIND \_ \_ TYPE**](capicom-certificate-find-type.md) que especifica o tipo de critérios de correspondência fornecidos no *parâmetro varCriteria.* A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH**</dt> </dl>                              | Retorna certificados com um hash SHA1 que corresponde ao hash SHA1 especificado no *parâmetro varCriteria.*<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**NOME DA ASSUNTO \_ DE \_ ENCONTRAR CERTIFICADO \_ \_ CAPICOM**</dt> </dl>                     | Retorna certificados cujo nome de assunto corresponde exatamente ou parcialmente ao nome da assunto especificado no *parâmetro varCriteria.* Essa chamada pesquisa apenas o campo nome da assunto.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**NOME DO EMISSOR DO CERTIFICADO CAPICOM \_ \_ FIND \_ \_**</dt> </dl>                        | Retorna certificados cujo nome do emissor corresponde exatamente ou parcialmente ao nome do emissor especificado no *parâmetro varCriteria.* Essa chamada pesquisa apenas o campo nome do emissor.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ ROOT \_ NAME**</dt> </dl>                              | Retorna certificados cujo nome de assunto raiz corresponde exatamente ou parcialmente ao nome da assunto raiz especificado no *parâmetro varCriteria.* Essa chamada cria uma cadeia. Essa chamada pesquisa o campo nome da assunto do certificado raiz.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**NOME DO MODELO \_ DE \_ ENCONTRAR CERTIFICADO \_ \_ CAPICOM**</dt> </dl>                  | Retorna certificados cujo nome de modelo corresponde ao nome do modelo especificado no *parâmetro varCriteria.*<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**EXTENSÃO CAPICOM \_ CERTIFICATE \_ FIND \_**</dt> </dl>                               | Retorna certificados que têm uma extensão que corresponde à extensão especificada no *parâmetro varCriteria.*<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**PROPRIEDADE ESTENDIDA \_ DE ENCONTRAR \_ CERTIFICADO \_ CAPICOM \_**</dt> </dl>      | Retorna certificados no armazenamento que contêm explicitamente uma propriedade estendida com o valor especificado no *parâmetro varCriteria.*<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**POLÍTICA DE APLICATIVO \_ DE ENCONTRAR \_ CERTIFICADO \_ CAPICOM \_**</dt> </dl>   | Retorna certificados no armazenamento que têm uma extensão de uso de chave aprimorada, extensão de política de aplicativo ou propriedade estendida especificada no *parâmetro varCriteria.*<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**POLÍTICA DE CERTIFICADO CAPICOM \_ \_ FIND \_ \_ CERTIFICATE**</dt> </dl>   | Retorna certificados que contêm o OID de política na extensão de Política de Certificado especificada no *parâmetro varCriteria.*<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**TEMPO DE ENCONTRE O CERTIFICADO CAPICOM \_ \_ \_ \_ VÁLIDO**</dt> </dl>                           | Retorna certificados cuja hora é válida.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**HORA DE LOCALIZAÇÃO DO CERTIFICADO CAPICOM \_ \_ AINDA NÃO \_ \_ \_ \_ VÁLIDA**</dt> </dl> | Retorna certificados cuja hora ainda não é válida.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**HORA DE LOCALIZAÇÃO DO CERTIFICADO CAPICOM \_ \_ \_ \_ EXPIRADO**</dt> </dl>                     | Retorna certificados cujo tempo expirou.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**USO DA CHAVE \_ DE ENCONTRAR CHAVE DO CERTIFICADO CAPICOM \_ \_ \_**</dt> </dl>                              | Retorna certificados que contêm usos de chave na extensão KeyUsage especificada no *parâmetro varCriteria.* Se a extensão KeyUsage não estiver presente, todos os usos de chave serão presumidos como indisponíveis.<br/>                           |



 

</dd> <dt>

*varCriteria* \[ in, opcional\]
</dt> <dd>

Uma variante que contém os critérios de pesquisa. Esses dados devem corresponder ao tipo de dados especificado no *parâmetro FindType.* Se o valor do parâmetro *FindType* for CAPICOM CERTIFICATE FIND TIME VALID, CAPICOM CERTIFICATE FIND TIME NOT YET VALID ou \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ CAPICOM \_ CERTIFICATE FIND TIME EXPIRED \_ \_ \_ e você não passar um valor para esse parâmetro, a hora atual será assumida. Para ver exemplos de cada tipo de dados, consulte Comentários. O valor padrão é 0.

</dd> <dt>

*bFindValidOnly* \[ in, opcional\]
</dt> <dd>

Um valor booliana que indica se apenas certificados válidos são retornados. O valor padrão é false; isso indica que todos os certificados que corresponderem aos critérios de pesquisa são retornados.

Se true, a pesquisa não retornará os seguintes tipos de certificados:

-   Certificados cuja hora expirou ou ainda não é válida.
-   Certificados não encadeados corretamente.
-   Certificados que têm problemas de assinatura.
-   Certificados revogados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

[**Objeto certificates**](certificates.md) que contém os resultados da pesquisa.

**CAPICOM 2.1:** O [**objeto Certificates**](certificates.md) retornado contém referências aos certificados na coleção na qual a pesquisa foi feita. Todas as alterações feitas nos certificados no objeto **Certificados** retornado são refletidas nessa coleção.

**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 e CAPICOM 2.0.0.3:** O [**objeto Certificates**](certificates.md) retornado contém cópias dos certificados na coleção na qual a pesquisa foi feita. As alterações feitas nos certificados no objeto **Certificados** retornado não são refletidas nessa coleção.

## <a name="remarks"></a>Comentários

Os exemplos a seguir mostram possíveis critérios de pesquisa para os diferentes tipos de critérios de pesquisa.



| *Parâmetro FindType*                              | *Parâmetro varCriteria*                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| NOME DA ASSUNTO \_ DE \_ ENCONTRAR CERTIFICADO \_ \_ CAPICOM         | "NameOfPerson"                                                                                                                     |
| NOME DO EMISSOR DO CERTIFICADO CAPICOM \_ \_ FIND \_ \_          | "VeriSign"                                                                                                                         |
| CAPICOM \_ CERTIFICATE \_ FIND \_ ROOT \_ NAME            | "Autoridade Raiz da Microsoft"                                                                                                         |
| NOME DO MODELO \_ DE \_ ENCONTRAR CERTIFICADO \_ \_ CAPICOM        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| EXTENSÃO CAPICOM \_ CERTIFICATE \_ FIND \_             | "2.5.29.31"<br/> EXTENSÃO DE USO \_ DE CHAVE OID CAPICOM \_ \_ \_<br/> "Lista de Distribuição de CRL"<br/>                           |
| PROPRIEDADE ESTENDIDA \_ DE ENCONTRAR \_ CERTIFICADO \_ CAPICOM \_    | CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO                                                                                                   |
| POLÍTICA DE APLICATIVO \_ DE ENCONTRAR \_ CERTIFICADO \_ CAPICOM \_   | "1.3.6.1.5.5.7.3.3"<br/> "1.3.6.1.5.5.7.3.4"<br/> CAPICOM \_ OID \_ SERVER \_ AUTH \_ EKU<br/> "Assinatura de código"<br/> |
| POLÍTICA DE CERTIFICADO CAPICOM \_ \_ FIND \_ \_ CERTIFICATE   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Corporate High Assurance"<br/>                                                           |
| TEMPO DE ENCONTRE O CERTIFICADO CAPICOM \_ \_ \_ \_ VÁLIDO           | \#15/04/2002, 18h\#                                                                                                            |
| HORA DE LOCALIZAÇÃO DO CERTIFICADO CAPICOM \_ \_ AINDA NÃO \_ \_ \_ \_ VÁLIDA | \#15/04/2002, 18h\#                                                                                                            |
| HORA DE LOCALIZAÇÃO DO CERTIFICADO CAPICOM \_ \_ \_ \_ EXPIRADO         | \#15/04/2002, 18h\#                                                                                                            |
| \_uso da \_ chave de localização de certificado CAPICOM \_ \_            | somente criptografia de capicos de \_ \_ \_ uso de chave \_                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificados**](certificates.md)
</dt> <dt>

[**OID de CAPICOM \_**](capicom-oid.md)
</dt> </dl>

 

 
