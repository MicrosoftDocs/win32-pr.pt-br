---
description: Recupera a coleção de certificados que está associada ao objeto SignedData. Depois de serem recuperados, os objetos de certificado individuais na coleção podem ser enumerados.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Propriedade SignedData. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758907"
---
# <a name="signeddatacertificates-property"></a>Propriedade SignedData. Certificates

\[A propriedade **Certificates** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **Certificates** recupera a coleção de [**certificados**](certificates.md) que está associada ao objeto [**SignedData**](signeddata.md) . Depois de serem recuperados, os objetos de [**certificado**](certificate.md) individuais na coleção podem ser enumerados.

## <a name="syntax"></a>Syntax


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a>Valor da propriedade

A coleção de [**certificados**](certificates.md) que está associada ao objeto [**SignedData**](signeddata.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
