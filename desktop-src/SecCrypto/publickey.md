---
description: O objeto PublicKey representa uma chave pública em um objeto de certificado.
title: Objeto PublicKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748864"
---
# <a name="publickey-object"></a>Objeto PublicKey

\[O objeto **PublicKey** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **PublicKey** representa uma chave pública em um objeto de [**certificado**](certificate.md) .

## <a name="when-to-use"></a>Quando usar

O objeto **PublicKey** é usado para recuperar dados sobre a chave pública.

## <a name="members"></a>Membros

O objeto **PublicKey** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **PublicKey** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso          | Descrição                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](publickey-algorithm.md)<br/>                 | Somente leitura<br/> | Recupera o objeto [**OID**](oid.md) que identifica o algoritmo usado pela chave pública. Essa é a propriedade padrão.<br/> |
| [**EncodedKey**](publickey-encodedkey.md)<br/>               | Somente leitura<br/> | Recupera um objeto [**EncodedData**](encodeddata.md) que fornece acesso ao valor da chave pública.<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | Somente leitura<br/> | Recupera um objeto [**EncodedData**](encodeddata.md) que fornece acesso aos parâmetros do algoritmo de chave pública.<br/>  |
| [**Comprimento**](publickey-length.md)<br/>                       | Somente leitura<br/> | Recupera o comprimento da chave pública em bits.<br/>                                                                             |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto **PublicKey** .

O objeto **PublicKey** é usado pelo método [**Certificate. PublicKey**](certificate-publickey.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
