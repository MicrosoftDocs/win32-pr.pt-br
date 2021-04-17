---
description: Recupera um valor booliano que indica se o bit keyEncipherment está definido.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: Propriedade KeyUsage. IsKeyEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787454"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a>Propriedade KeyUsage. IsKeyEnciphermentEnabled

\[A propriedade **IsKeyEnciphermentEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **IsKeyEnciphermentEnabled** recupera um valor booliano que indica se o bit keyEncipherment está definido.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for **true**, o bit keyEncipherment será definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Uso de**](keyusage.md)
</dt> </dl>

 

 
