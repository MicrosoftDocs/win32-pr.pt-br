---
description: Recupera o local do repositório de certificados que este objeto representa.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Propriedade Store. Location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752739"
---
# <a name="storelocation-property"></a>Propriedade Store. Location

\[A propriedade **Location** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Location** recupera o local do repositório de certificados que este objeto representa.

## <a name="syntax"></a>Syntax


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valor da propriedade

O valor do [**\_ \_ local do armazenamento CAPICOM**](capicom-store-location.md) que representa o local do repositório de certificados.

## <a name="remarks"></a>Comentários

O valor da propriedade **Location** é o mesmo que o valor fornecido para o parâmetro *StoreLocation* do método [**Open**](store-open.md) quando o armazenamento foi aberto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Repositório**](store.md)
</dt> </dl>

 

 
