---
description: Retorna um valor booliano que indica se a extensão EKU está marcada como crítica.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: Propriedade ExtendedKeyUsage. iscriticable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a5e5b52d0901222ae3dbf7daac87be2d59a90152c9aa4e0a78f023af1a6848a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007384"
---
# <a name="extendedkeyusageiscritical-property"></a>Propriedade ExtendedKeyUsage. iscriticable

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Iscriticad** retorna um valor booliano que indica se a extensão EKU está marcada como crítica.

## <a name="syntax"></a>Syntax


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **for true**, a extensão EKU será marcada como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ExtendedKeyUsage**](extendedkeyusage.md)
</dt> </dl>

 

 
