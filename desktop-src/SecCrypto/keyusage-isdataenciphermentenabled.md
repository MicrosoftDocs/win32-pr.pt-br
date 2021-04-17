---
description: Recupera um valor booliano que indica se o bit dataEncipherment está definido.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: Propriedade KeyUsage. IsDataEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aad6cbcd21830ad127b9537749dfb1c05a4c9ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813105"
---
# <a name="keyusageisdataenciphermentenabled-property"></a>Propriedade KeyUsage. IsDataEnciphermentEnabled

\[A propriedade **IsDataEnciphermentEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **IsDataEnciphermentEnabled** recupera um valor booliano que indica se o bit dataEncipherment está definido.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for **true**, o bit dataEncipherment será definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Uso de**](keyusage.md)
</dt> </dl>

 

 
