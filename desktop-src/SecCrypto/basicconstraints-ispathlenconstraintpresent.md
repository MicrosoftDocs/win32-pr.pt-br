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
ms.openlocfilehash: 9809b6747bac548b14b37384719dbe2660188582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758923"
---
# <a name="basicconstraintsispathlenconstraintpresent-property"></a>Propriedade BasicConstraints. IsPathLenConstraintPresent

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

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
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
