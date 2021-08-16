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
ms.openlocfilehash: 3918a89719195e6c8672a0dab13c62af3e866f8fd5695df20f0126f7831f369c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773028"
---
# <a name="basicconstraintsiscritical-property"></a>Propriedade BasicConstraints. iscriticable

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

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
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
