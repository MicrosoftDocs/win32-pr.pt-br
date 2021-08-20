---
description: Contém informações sobre como construir uma cadeia de certificados confiáveis.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Objeto CertificateStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c0c228a06da9d0a4dd93491908af0c0a2d0693125be57b675ca64e10378f253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769986"
---
# <a name="certificatestatus-object"></a>Objeto CertificateStatus

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **CertificateStatus** contém informações sobre como construir uma cadeia de certificados confiáveis.

## <a name="members"></a>Membros

O objeto **CertificateStatus** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **CertificateStatus** tem esses métodos.



| Método                                                               | Descrição                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](certificatestatus-applicationpolicies.md) | Retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de aplicativo.<br/>                                           |
| [**CertificatePolicies**](certificatestatus-certificatepolicies.md) | Retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de certificado usados durante a criação de cadeia.<br/>                |
| [**EKU**](certificatestatus-eku.md)                                 | Retorna o objeto [**EKU**](eku.md) usado para definir os elementos EKU a serem verificados no estabelecimento do status de validade de um certificado.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **CertificateStatus** tem essas propriedades.



| Propriedade                                                                        | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](certificatestatus-certificates.md)<br/>               | Leitura/gravação<br/> | Define ou recupera a coleção de certificados que podem ser usados para criar a cadeia de certificados.<br/> **CAPICOM 2.0.0.3 e anteriores:** Não há suporte para a propriedade [**Certificates**](certificatestatus-certificates.md) .<br/>                    |
| [**CheckFlag**](certificatestatus-checkflag.md)<br/>                     | Leitura/gravação<br/> | Sinalizador de verificação de validade. Os valores podem ser Unidos usando um operador **or** lógico. O sinalizador de verificação padrão é [**Capicot \_ verificar \_ \_ tudo online**](capicom-check-flag.md).<br/>                                                                                     |
| [**Resultado**](certificatestatus-result.md)<br/>                           | Somente leitura<br/>  | Indica se o certificado é válido. A validade do certificado é verificada usando a configuração atual da propriedade [**CheckFlag**](certificatestatus-checkflag.md) e as configurações de política do certificado. Essa é a propriedade padrão.<br/> |
| [**UrlRetrievalTimeout**](certificatestatus-urlretrievaltimeout.md)<br/> | Leitura/gravação<br/> | Define ou recupera o período de tempo antes que uma URL seja determinada como inacessível.<br/>                                                                                                                                                                     |
| [**Verificação de**](certificatestatus-verificationtime.md)<br/>       | Leitura/gravação<br/> | Define ou recupera a hora em que o certificado foi verificado.<br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

O objeto **CertificateStatus** não pode ser criado.

O objeto **CertificateStatus** é retornado pelo método [**Certificate. IsValid**](certificate-isvalid.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**Cadeia**](chain.md)
</dt> </dl>

 

 
