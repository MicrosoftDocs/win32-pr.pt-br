---
description: Recupera um valor booliano que indica se a extensão de restrição básica está marcada como crítica.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: Propriedade BasicConstraints. iscriticable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8f3f61a0c458229977abae60258ba4cb71420e72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762907"
---
# <a name="basicconstraintsiscritical-property"></a>Propriedade BasicConstraints. iscriticable

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

A propriedade **Iscriticat** recupera um valor booliano que indica se a extensão de restrição básica está marcada como crítica.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **for true**, a extensão de restrição básica será marcada como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
