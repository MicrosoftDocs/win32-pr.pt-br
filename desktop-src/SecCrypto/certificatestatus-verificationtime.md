---
description: Define ou recupera a hora em que o certificado foi verificado.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Propriedade CertificateStatus. Verification
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
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760016"
---
# <a name="certificatestatusverificationtime-property"></a>Propriedade CertificateStatus. Verification

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **verificatime** define ou recupera a hora em que o certificado foi verificado.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a>Valor da propriedade

A hora em que o certificado foi verificado.

## <a name="remarks"></a>Comentários

Se essa propriedade não for definida, a hora atual será usada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
