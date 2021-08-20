---
description: A propriedade Certificates recupera uma coleção de Certificados que representa os certificados na cadeia. Essa é a propriedade padrão.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: Propriedade IChain2::Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16fb08d020dcd59ed7caf22a0e93f4a4866b58642f12d0c131f3f0368bd3e7e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769647"
---
# <a name="ichain2certificates-property"></a>Propriedade IChain2::Certificates

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade Certificates** recupera uma [**coleção de Certificados**](certificates.md) que representa os certificados na cadeia. Essa é a propriedade padrão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>Valor da propriedade

Uma [**coleção de Certificados**](certificates.md) usada para recuperar informações sobre cada certificado na cadeia. O primeiro certificado na coleção retornada, **Certificates.Item**(1), é o certificado final da cadeia. O último certificado na coleção, **Certificates.Item**(**Certificates.Count),** é o [*certificado raiz*](../secgloss/r-gly.md) da cadeia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
