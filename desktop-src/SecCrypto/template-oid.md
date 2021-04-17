---
description: Recupera um objeto OID que identifica o objeto de modelo.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Propriedade Template. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752738"
---
# <a name="templateoid-property"></a>Propriedade Template. OID

\[A propriedade **OID** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]

A propriedade **OID** recupera um objeto [**OID**](oid.md) que identifica o objeto de [**modelo**](template.md) .

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Template.OID As OID
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**OID**](oid.md) que identifica o objeto de [**modelo**](template.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Modelo**](template.md)
</dt> </dl>

 

 
