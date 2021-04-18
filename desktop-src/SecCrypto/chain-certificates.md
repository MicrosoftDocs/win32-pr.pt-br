---
description: A propriedade Certificates recupera uma coleção de certificados que representa os certificados na cadeia. Essa é a propriedade padrão.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'Propriedade IChain2:: Certificates'
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
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756377"
---
# <a name="ichain2certificates-property"></a>Propriedade IChain2:: Certificates

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Certificates** recupera uma coleção de [**certificados**](certificates.md) que representa os certificados na cadeia. Essa é a propriedade padrão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>Valor da propriedade

Uma coleção de [**certificados**](certificates.md) que é usada para recuperar informações sobre cada certificado na cadeia. O primeiro certificado na coleção retornada, **Certificates. Item**(1), é o certificado final da cadeia. O último certificado na coleção, **Certificates. Item**(**Certificates. Count**), é o [*certificado raiz*](../secgloss/r-gly.md) da cadeia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
