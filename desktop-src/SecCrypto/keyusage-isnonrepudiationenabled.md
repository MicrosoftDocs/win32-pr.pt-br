---
description: Recupera um valor booliano que indica se o bit nonRepudiationEnabled está definido.
ms.assetid: d9bcf0fc-8b2d-408c-b587-71903ef5f5f6
title: Propriedade KeyUsage.IsNonRepudiationEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsNonRepudiationEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7b5ba81aad49a33a987b2c16c072a6666776b665bf1bd936086a25d1ddd542f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408726"
---
# <a name="keyusageisnonrepudiationenabled-property"></a>Propriedade KeyUsage.IsNonRepudiationEnabled

\[A **propriedade IsNonRepudiationEnabled** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade IsNonRepudiationEnabled** recupera um valor booliano que indica se o bit nãoRepudiationEnabled está definido.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsNonRepudiationEnabled As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **true**, o bit nonRepudiationEnabled será definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
