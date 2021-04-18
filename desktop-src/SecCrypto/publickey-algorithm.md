---
description: A propriedade Algorithm recupera o objeto OID que identifica o algoritmo usado pela chave pública. Essa é a propriedade padrão.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: Propriedade PublicKey. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753396"
---
# <a name="publickeyalgorithm-property"></a>Propriedade PublicKey. Algorithm

\[A propriedade de **algoritmo** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Algorithm** recupera o objeto [**OID**](oid.md) que identifica o algoritmo usado pela chave pública. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a>Valor da propriedade

O objeto [**OID**](oid.md) que identifica o algoritmo usado pela chave pública.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
