---
description: Define ou recupera o período de tempo antes que uma URL seja determinada como inacessível.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: Propriedade CertificateStatus. UrlRetrievalTimeout
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b56e9bca2cc7c666f980df8905ac79fc885050d37359e524a83e287dcd5415e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770086"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a>Propriedade CertificateStatus. UrlRetrievalTimeout

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **UrlRetrievalTimeout** define ou recupera o período de tempo antes que uma URL seja determinada como inacessível.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de segundos antes que uma URL seja determinada como inacessível.

## <a name="remarks"></a>Comentários

Se essa propriedade não for definida, o tempo limite padrão será de 15 segundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
