---
description: Recupera uma coleção dos qualificadores da política.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: Propriedade PolicyInformation. Qualifiers (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811050"
---
# <a name="policyinformationqualifiers-property"></a>Propriedade PolicyInformation. Qualifiers

\[A propriedade **Qualifiers** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar informações de política na extensão de políticas de certificado.\]

A propriedade **Qualifiers** recupera uma coleção dos qualificadores da política.

## <a name="syntax"></a>Syntax


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a>Valor da propriedade

O ponteiro do CPS (instrução de prática de certificação) da política ou os qualificadores de aviso do usuário, como um objeto de [**qualificadores**](qualifiers.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| parâmetro<br/>          | <dl> <dt>IADs. h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
