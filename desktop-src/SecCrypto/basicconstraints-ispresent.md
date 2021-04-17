---
description: Recupera um valor booliano que indica se a extensão de restrições básica está presente. Essa é a propriedade padrão.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: Propriedade BasicConstraints. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9632f0d1297f2effd7d1bcc6056b2327d7f38e26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751076"
---
# <a name="basicconstraintsispresent-property"></a>Propriedade BasicConstraints. IsPresent

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

A propriedade **IsPresent** recupera um valor booliano que indica se a extensão de restrições básicas está presente. Essa é a propriedade padrão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for **true**, a extensão de restrições básicas estará presente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BasicConstraints**](basicconstraints.md)
</dt> </dl>

 

 
