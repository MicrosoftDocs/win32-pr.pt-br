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
ms.openlocfilehash: b6c19acc094426f99599b9e4aa9ea3968414c7de1d99377b2ce0bd2e8e3fde05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877986"
---
# <a name="certificate-object"></a>Objeto de certificado

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **objeto** Certificate representa um único [*certificado digital.*](../secgloss/d-gly.md)

O **objeto** Certificate expõe as seguintes interfaces:

-   **ICertificate** – introduzido no CAPICOM 1.0.
-   **ICertificate2** – introduzido no CAPICOM 2.0.

## <a name="when-to-use"></a>Quando usar

O **objeto** Certificate é usado para executar as seguintes tarefas:

-   Carregar dados de certificado, incluindo a chave privada, de um arquivo.
-   Obter informações do certificado.
-   Retornar restrições básicas, EKU, propriedades estendidas, extensões, uso de chave, chave pública e objetos de modelo associados ao certificado.
-   Determine se o certificado é válido e verifique a disponibilidade de acesso da chave privada da entidade do certificado.
-   Exibir o certificado.
-   Importe e exporte o certificado.
-   Salve o certificado em um arquivo.
-   Recuperar ou definir propriedades que descrevem o certificado.

## <a name="members"></a>Membros

O **objeto** Certificate tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto** Certificate tem esses métodos.



| Método                                                       | Descrição                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BasicConstraints**](certificate-basicconstraints.md)     | Retorna um [**objeto BasicConstraints**](basicconstraints.md) que representa a extensão de restrições básicas do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)                                                   |
| [**Exibir**](certificate-display.md)                       | Exibe um certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)                                                                                                                                                             |
| [**Exportação**](certificate-export.md)                         | Copia um certificado para uma cadeia de caracteres codificada. A cadeia de caracteres codificada pode ser escrita em um arquivo ou importada em um novo **objeto Certificate.**<br/> (Herdado **de CertificateICertificate2ICertificate**)                                               |
| [**ExtendedKeyUsage**](certificate-extendedkeyusage.md)     | Retorna um [**objeto ExtendedKeyUsage**](extendedkeyusage.md) que indica os usos válidos de chave estendida do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)                                                       |
| [**Extendedproperties**](certificate-extendedproperties.md) | Retorna uma coleção das propriedades estendidas do certificado.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                             |
| [**Extensões**](certificate-extensions.md)                 | Retorna uma coleção das extensões associadas ao certificado.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                         |
| [**GetInfo**](certificate-getinfo.md)                       | Recupera informações do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)                                                                                                                                         |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | Determina se o certificado tem [*uma chave privada*](../secgloss/p-gly.md) associada a ele.<br/> (Herdado **de CertificateICertificate2ICertificate**)                                    |
| [**Importar**](certificate-import.md)                         | Importa um certificado codificado anteriormente de uma cadeia de caracteres para o **objeto Certificate.**<br/> (Herdado **de CertificateICertificate2ICertificate**)                                                                                             |
| [**IsValid**](certificate-isvalid.md)                       | Cria uma cadeia de verificação de certificado para um certificado e retorna um [**objeto CertificateStatus**](certificatestatus.md) que contém o status de validade do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**) |
| [**KeyUsage**](certificate-keyusage.md)                     | Retorna um [**objeto KeyUsage**](keyusage.md) que indica o uso de chave válido do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)                                                                                |
| [**Carregar**](certificate-load.md)                             | Importa um certificado de um arquivo.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                                                              |
| [**Publickey**](certificate-publickey.md)                   | Retorna um [**objeto PublicKey.**](publickey.md)<br/> (Herdado de **CertificateICertificate2**)                                                                                                                                                |
| [**Salvar**](certificate-save.md)                             | Salva o certificado em um arquivo.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                                                                |
| [**Modelo**](certificate-template.md)                     | Retorna o modelo associado ao certificado.<br/> (Herdado de **CertificateICertificate2**)                                                                                                                                           |



 

### <a name="properties"></a>Propriedades

O **objeto Certificate** tem essas propriedades.



| Propriedade                                                      | Tipo de acesso           | Descrição                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Arquivado**](certificate-archived.md)<br/>           | Leitura/gravação<br/> | Define ou recupera um valor booliana que indica se o certificado está arquivado.<br/> (Herdado de **CertificateICertificate2**)       |
| [**IssuerName**](certificate-issuername.md)<br/>       | Somente leitura<br/>  | Recupera uma cadeia de caracteres que contém o nome do emissor do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)            |
| [**Privatekey**](certificate-privatekey.md)<br/>       | Leitura/gravação<br/> | Define ou recupera a chave privada associada ao certificado.<br/> (Herdado de **CertificateICertificate2**)                          |
| [**Serialnumber**](certificate-serialnumber.md)<br/>   | Somente leitura<br/>  | Recupera uma cadeia de caracteres que contém o número de série do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)                 |
| [**SubjectName**](certificate-subjectname.md)<br/>     | Somente leitura<br/>  | Recupera uma cadeia de caracteres que contém o nome da pessoa do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)           |
| [**Impressão Digital**](certificate-thumbprint.md)<br/>       | Somente leitura<br/>  | Recupera uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**) |
| [**ValidFromDate**](certificate-validfromdate.md)<br/> | Somente leitura<br/>  | Recupera a data de início para a validade do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)               |
| [**ValidToDate**](certificate-validtodate.md)<br/>     | Somente leitura<br/>  | Recupera a data de término para a validade do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)                  |
| [**Versão**](certificate-version.md)<br/>             | Somente leitura<br/>  | Recupera o número de versão do certificado.<br/> (Herdado **de CertificateICertificate2ICertificate**)                                |



 

## <a name="remarks"></a>Comentários

O **objeto** Certificate pode ser criado e é seguro para scripts. O ProgID para o **objeto Certificate** é "CAPICOM. Certificate.2".

**CAPICOM 1. *x*:** o ProgID para o **objeto Certificate** é "CAPICOM. Certificate.1".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
