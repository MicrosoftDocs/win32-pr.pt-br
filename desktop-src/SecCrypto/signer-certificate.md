---
description: Define ou recupera o objeto de certificado que representa o certificado de um signatário dos dados.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Propriedade signatário. Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811048"
---
# <a name="signercertificate-property"></a>Propriedade signatário. Certificate

\[A propriedade de **certificado** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade de **certificado** define ou recupera o objeto de [**certificado**](certificate.md) que representa o certificado de um signatário dos dados. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a>Valor da propriedade

O objeto de [**certificado**](certificate.md) que representa o certificado de um signatário dos dados.

## <a name="remarks"></a>Comentários

Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Signatário**](signer.md)
</dt> </dl>

 

 
