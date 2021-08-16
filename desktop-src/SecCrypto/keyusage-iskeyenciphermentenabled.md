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
ms.openlocfilehash: 75d1c8f90712b41f7e489b333e49b7e96b48825d33f82d85e37813f5046ace26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622286"
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
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Uso de**](keyusage.md)
</dt> </dl>

 

 
