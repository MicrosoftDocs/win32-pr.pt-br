---
description: Recupera o objeto PolicyInformation que representa a política indexada. Essa é a propriedade padrão.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: Propriedade CertificatePolicies. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758167"
---
# <a name="certificatepoliciesitem-property"></a>Propriedade CertificatePolicies. Item

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para as políticas de certificado para recuperar as políticas de certificado.\]

A propriedade **Item** recupera o objeto [**PolicyInformation**](policyinformation.md) que representa a política indexada. Essa é a propriedade padrão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**PolicyInformation**](policyinformation.md) que representa a política indexada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
