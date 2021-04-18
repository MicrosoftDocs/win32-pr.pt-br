---
description: Recupera o nome do repositório de certificados que este objeto representa.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Propriedade Store.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751513"
---
# <a name="storename-property"></a>Propriedade Store.Name

\[A propriedade [**Name**](store-location.md) está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade [**Name**](store-location.md) recupera o nome do repositório de certificados que este objeto representa.

## <a name="syntax"></a>Syntax


```VB
Store.Name As String
```



## <a name="property-value"></a>Valor da propriedade

O valor da **cadeia de caracteres** que representa o nome do repositório de certificados.

## <a name="remarks"></a>Comentários

Exemplos de nomes de repositório de certificados incluem My e root.

O valor da propriedade [**Name**](store-location.md) é o mesmo que o valor fornecido para o parâmetro *StoreName* do método [**Open**](store-open.md) quando o armazenamento foi aberto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Repositório**](store.md)
</dt> </dl>

 

 
