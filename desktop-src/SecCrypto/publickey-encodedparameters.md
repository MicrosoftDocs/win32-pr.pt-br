---
description: Recupera os parâmetros do algoritmo de chave pública.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: Propriedade PublicKey. EncodedParameters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811789"
---
# <a name="publickeyencodedparameters-property"></a>Propriedade PublicKey. EncodedParameters

\[A propriedade **EncodedParameters** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **EncodedParameters** recupera os parâmetros do algoritmo de chave pública.

## <a name="syntax"></a>Syntax


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**EncodedData**](encodeddata.md) que fornece acesso aos parâmetros do algoritmo de chave pública.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
