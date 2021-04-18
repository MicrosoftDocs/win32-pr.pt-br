---
description: Recupera o número de objetos PolicyInformation na coleção.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: Propriedade CertificatePolicies. Count
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
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758168"
---
# <a name="certificatepoliciescount-property"></a>Propriedade CertificatePolicies. Count

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para as políticas de certificado para recuperar as políticas de certificado.\]

A propriedade **Count** recupera o número de objetos [**PolicyInformation**](policyinformation.md) na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de objetos [**PolicyInformation**](policyinformation.md) na coleção. Cada objeto **PolicyInformation** representa uma única política de certificado na coleção.

## <a name="remarks"></a>Comentários

A propriedade **Count** pode ser usada para especificar o último objeto [**PolicyInformation**](policyinformation.md) na coleção ao recuperar um objeto **PolicyInformation** específico usando a propriedade [**CertificatePolicies. Item**](certificatepolicies-item.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
