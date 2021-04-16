---
description: Recupera um valor booliano que indica se a extensão KeyUsage está presente.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: Propriedade keyutilization. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750752"
---
# <a name="keyusageispresent-property"></a>Propriedade keyutilization. IsPresent

\[A propriedade **IsPresent** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **IsPresent** recupera um valor booliano que indica se a extensão [**KeyUsage**](keyusage.md) está presente.

Essa propriedade é a propriedade padrão do objeto [**KeyUsage**](keyusage.md) .

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for **true**, a extensão KeyUsage estará presente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Uso de**](keyusage.md)
</dt> </dl>

 

 
