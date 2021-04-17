---
description: Recupera um valor booliano que indica se o bit keyCertSign está definido.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: Propriedade KeyUsage. IsKeyCertSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761863"
---
# <a name="keyusageiskeycertsignenabled-property"></a>Propriedade KeyUsage. IsKeyCertSignEnabled

\[A propriedade **IsKeyCertSignEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **IsKeyCertSignEnabled** recupera um valor booliano que indica se o bit keyCertSign está definido.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for **true**, o bit keyCertSign será definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Uso de**](keyusage.md)
</dt> </dl>

 

 
