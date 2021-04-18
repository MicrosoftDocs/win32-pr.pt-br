---
description: Define ou recupera a coleção de certificados que podem ser usados para criar a cadeia de certificados.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: Propriedade CertificateStatus. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756154"
---
# <a name="certificatestatuscertificates-property"></a>Propriedade CertificateStatus. Certificates

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Certificates** define ou recupera a coleção de certificados que pode ser usada para criar a cadeia de certificados.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a>Valor da propriedade

Um objeto de [**certificados**](certificates.md) que representa a coleção de certificados que podem ser usados para criar a cadeia de certificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
