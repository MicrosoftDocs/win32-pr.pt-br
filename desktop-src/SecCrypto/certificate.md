---
description: Representa um único certificado digital.
ms.assetid: da95312b-cc9f-44f0-9517-0b28c5fcfb61
title: Objeto de certificado
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1360b197f0d7f5e0579a5378a37047e6a117a9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758018"
---
# <a name="certificate-object"></a>Objeto de certificado

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto de **certificado** representa um único [*certificado digital*](../secgloss/d-gly.md).

O objeto de **certificado** expõe as seguintes interfaces:

-   **ICertificate** — introduzido no capicom 1,0.
-   **ICertificate2** — introduzido no capicom 2,0.

## <a name="when-to-use"></a>Quando usar

O objeto de **certificado** é usado para executar as seguintes tarefas:

-   Carregue os dados do certificado, incluindo a chave privada, de um arquivo.
-   Obter informações do certificado.
-   Retornar restrições básicas, EKU, propriedades estendidas, extensões, uso de chave, chave pública e objetos de modelo associados ao certificado.
-   Determine se o certificado é válido e verifique a disponibilidade de acesso da chave privada da entidade do certificado.
-   Exibir o certificado.
-   Importe e exporte o certificado.
-   Salve o certificado em um arquivo.
-   Recupere ou defina as propriedades que descrevem o certificado.

## <a name="members"></a>Membros

O objeto de **certificado** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto de **certificado** tem esses métodos.



| Método                                                       | Descrição                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BasicConstraints**](certificate-basicconstraints.md)     | Retorna um objeto [**BasicConstraints**](basicconstraints.md) que representa a extensão de restrições básicas do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)                                                   |
| [**Monitor**](certificate-display.md)                       | Exibe um certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)                                                                                                                                                             |
| [**Exportação**](certificate-export.md)                         | Copia um certificado para uma cadeia de caracteres codificada. A cadeia de caracteres codificada pode ser gravada em um arquivo ou importada para um novo objeto de **certificado** .<br/> (Herdado de **CertificateICertificate2ICertificate**)                                               |
| [**ExtendedKeyUsage**](certificate-extendedkeyusage.md)     | Retorna um objeto [**ExtendedKeyUsage**](extendedkeyusage.md) que indica os usos válidos de chave estendida do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)                                                       |
| [**ExtendedProperties**](certificate-extendedproperties.md) | Retorna uma coleção das propriedades estendidas do certificado.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                             |
| [**Extensões**](certificate-extensions.md)                 | Retorna uma coleção das extensões associadas ao certificado.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                         |
| [**GetInfo**](certificate-getinfo.md)                       | Recupera informações do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)                                                                                                                                         |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | Determina se o certificado tem uma [*chave privada*](../secgloss/p-gly.md) associada a ele.<br/> (Herdado de **CertificateICertificate2ICertificate**)                                    |
| [**Importar**](certificate-import.md)                         | Importa um certificado codificado anteriormente de uma cadeia de caracteres para o objeto de **certificado** .<br/> (Herdado de **CertificateICertificate2ICertificate**)                                                                                             |
| [**IsValid**](certificate-isvalid.md)                       | Cria uma cadeia de verificação de certificado para um certificado e retorna um objeto [**CertificateStatus**](certificatestatus.md) que contém o status de validade do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**) |
| [**Uso de**](certificate-keyusage.md)                     | Retorna um objeto [**KeyUsage**](keyusage.md) que indica o uso de chave válido do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)                                                                                |
| [**Carregar**](certificate-load.md)                             | Importa um certificado de um arquivo.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                                                              |
| [**PublicKey**](certificate-publickey.md)                   | Retorna um objeto [**PublicKey**](publickey.md) .<br/> (Herdado de **CertificateICertificate2**)                                                                                                                                                |
| [**Salvar**](certificate-save.md)                             | Salva o certificado em um arquivo.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                                                                |
| [**Modelo**](certificate-template.md)                     | Retorna o modelo associado ao certificado.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                                           |



 

### <a name="properties"></a>Propriedades

O objeto de **certificado** tem essas propriedades.



| Propriedade                                                      | Tipo de acesso           | Descrição                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Arquivado**](certificate-archived.md)<br/>           | Leitura/gravação<br/> | Define ou recupera um valor booliano que indica se o certificado está arquivado.<br/> (Herdado de **CertificateICertificate2**)       |
| [**IssuerName**](certificate-issuername.md)<br/>       | Somente leitura<br/>  | Recupera uma cadeia de caracteres que contém o nome do emissor do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)            |
| [**PrivateKey**](certificate-privatekey.md)<br/>       | Leitura/gravação<br/> | Define ou recupera a chave privada associada ao certificado.<br/> (Herdado de **CertificateICertificate2**)                          |
| [**SerialNumber**](certificate-serialnumber.md)<br/>   | Somente leitura<br/>  | Recupera uma cadeia de caracteres que contém o número de série do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)                 |
| [**SubjectName**](certificate-subjectname.md)<br/>     | Somente leitura<br/>  | Recupera uma cadeia de caracteres que contém o nome da entidade do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)           |
| [**Impressão digital**](certificate-thumbprint.md)<br/>       | Somente leitura<br/>  | Recupera uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**) |
| [**ValidFromDate**](certificate-validfromdate.md)<br/> | Somente leitura<br/>  | Recupera a data de início da validade do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)               |
| [**ValidToDate**](certificate-validtodate.md)<br/>     | Somente leitura<br/>  | Recupera a data de término da validade do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)                  |
| [**Versão**](certificate-version.md)<br/>             | Somente leitura<br/>  | Recupera o número de versão do certificado.<br/> (Herdado de **CertificateICertificate2ICertificate**)                                |



 

## <a name="remarks"></a>Comentários

O objeto de **certificado** pode ser criado e é seguro para scripts. O ProgID do objeto de **certificado** é "CAPICOM. Certificado. 2 ".

**CAPICOM 1. *x*:** o ProgID para o objeto de **certificado** é "CAPICOM. Certificate. 1 ".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
