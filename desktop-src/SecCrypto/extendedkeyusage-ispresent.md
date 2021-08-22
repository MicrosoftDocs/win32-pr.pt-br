---
description: Retorna um valor booliano que indica se a extensão EKU está presente. Essa é a propriedade padrão.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: Propriedade ExtendedKeyUsage. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43c561e6c848380326151af12aebf584fb53eb7332c8e6c0d61074da03f7d3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007334"
---
# <a name="extendedkeyusageispresent-property"></a>Propriedade ExtendedKeyUsage. IsPresent

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **IsPresent** retorna um valor booliano que indica se a extensão EKU está presente. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for **true**, a extensão EKU estará presente.

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

 

 
