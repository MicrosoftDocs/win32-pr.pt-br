---
description: Recupera o número de objetos PolicyInformation na coleção.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: Propriedade CertificatePolicies.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 405fbc928f6ff553abe3cd55d3f6e08a1aed13ef46093f912b6b08af45ec2c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771040"
---
# <a name="certificatepoliciescount-property"></a>Propriedade CertificatePolicies.Count

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**Classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para Políticas de Certificado para recuperar as políticas de certificado.\]

A **propriedade Count** recupera o número de objetos [**PolicyInformation**](policyinformation.md) na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de [**objetos PolicyInformation**](policyinformation.md) na coleção. Cada **objeto PolicyInformation** representa uma única política de certificado na coleção.

## <a name="remarks"></a>Comentários

A **propriedade Count** pode ser usada para especificar o último objeto [**PolicyInformation**](policyinformation.md) na coleção ao recuperar um objeto **PolicyInformation** específico usando a propriedade [**CertificatePolicies.Item.**](certificatepolicies-item.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
