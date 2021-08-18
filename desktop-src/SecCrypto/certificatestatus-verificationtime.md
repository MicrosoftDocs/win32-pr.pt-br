---
description: Define ou recupera a hora em que o certificado foi verificado.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Propriedade CertificateStatus.VerificationTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 02457355fdb9f01605470ea10e30d69caaa6149837480ebe7bd20340d7c6cae2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993146"
---
# <a name="certificatestatusverificationtime-property"></a>Propriedade CertificateStatus.VerificationTime

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade VerificationTime** define ou recupera a hora em que o certificado foi verificado.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a>Valor da propriedade

A hora em que o certificado foi verificado.

## <a name="remarks"></a>Comentários

Se essa propriedade não estiver definida, a hora atual será usada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
