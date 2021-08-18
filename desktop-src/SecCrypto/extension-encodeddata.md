---
description: Recupera os dados codificados para a extensão.
ms.assetid: 79811557-6d7e-4d19-bcbb-1f79455dd286
title: Propriedade Extension.EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4783a6f598bf094ca2bca10b2abcb7e222e34ffc5956b2dc6f0977416e9e99a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006944"
---
# <a name="extensionencodeddata-property"></a>Propriedade Extension.EncodedData

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade EncodedData** recupera os dados codificados para a extensão.

## <a name="syntax"></a>Syntax


```VB
Extension.EncodedData As EncodedData
```



## <a name="property-value"></a>Valor da propriedade

Um [**objeto EncodedData**](encodeddata.md) que representa os dados da extensão de certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
