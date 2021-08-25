---
description: Recupera um valor booliano que indica se a restrição de comprimento de caminho está presente.
ms.assetid: 25840a62-13d1-4b54-9b09-64f77a465e06
title: Propriedade BasicConstraints. IsPathLenConstraintPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPathLenConstraintPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c6faf267508476f423efaff6b012a25114eca25e7bc21c51c51b9a3e66dde802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879726"
---
# <a name="basicconstraintsispathlenconstraintpresent-property"></a>Propriedade BasicConstraints. IsPathLenConstraintPresent

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

A propriedade **IsPathLenConstraintPresent** recupera um valor booliano que indica se a restrição de comprimento do caminho está presente.

## <a name="syntax"></a>Syntax


```VB
BasicConstraints.IsPathLenConstraintPresent As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for **true**, a restrição de comprimento do caminho estará presente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
