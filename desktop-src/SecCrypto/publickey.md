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
ms.openlocfilehash: 5d27a89d51840e70563854b3cc7f9084b6bd42cb5707630755e771d610c64a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901343"
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
| [**Muito**](publickey-length.md)<br/>                       | Somente leitura<br/> | Recupera o comprimento da chave pública em bits.<br/>                                                                             |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto **PublicKey** .

O objeto **PublicKey** é usado pelo método [**Certificate. PublicKey**](certificate-publickey.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
