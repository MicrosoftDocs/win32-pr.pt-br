---
description: Recupera um valor booliana que indica se o bit keyCertSign está definido.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: Propriedade KeyUsage.IsKeyCertSignEnabled
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
ms.openlocfilehash: 61c5ca1e9ae36159293e1e9afe1f79b5ff30cbd659b01a400797ae35aac8873c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515876"
---
# <a name="keyusageiskeycertsignenabled-property"></a>Propriedade KeyUsage.IsKeyCertSignEnabled

\[A **propriedade IsKeyCertSignEnabled** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade IsKeyCertSignEnabled** recupera um valor booliana que indica se o bit keyCertSign está definido.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **true**, o bit keyCertSign será definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
