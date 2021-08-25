---
description: Recupera um valor booliana que indica se o certificado é para uma AC (autoridade de certificação).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: Propriedade BasicConstraints.IsCertificateAuthority
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 90d616f4a7a0fe8522118848826bee88523ad45c34cb8a3fff23c722e68f2495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879756"
---
# <a name="basicconstraintsiscertificateauthority-property"></a>Propriedade BasicConstraints.IsCertificateAuthority

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, [**use a Classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

A **propriedade IsCertificateAuthority** recupera um valor booliana que indica se o certificado é para uma AC (autoridade [*de*](../secgloss/c-gly.md) certificação).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **True**, o certificado deve ser usado somente por uma AC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
