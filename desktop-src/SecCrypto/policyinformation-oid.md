---
description: Recupera o OID da política. Essa é a propriedade padrão.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Propriedade PolicyInformation. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800079"
---
# <a name="policyinformationoid-property"></a>Propriedade PolicyInformation. OID

\[A propriedade **OID** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar informações de política na extensão de políticas de certificado.\]

A propriedade **OID** recupera o OID da política. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a>Valor da propriedade

O identificador de objeto da política como um objeto de [**OID**](oid.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
