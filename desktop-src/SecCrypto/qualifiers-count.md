---
description: Recupera o número de objetos de qualificador na coleção.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Propriedade qualifierrs. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fd4cfe0d600c99251db77b1764edb83353b01143fc5179c1efc29673e30e734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900942"
---
# <a name="qualifierscount-property"></a>Propriedade qualifierrs. Count

\[A propriedade **Count** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]

A propriedade **Count** recupera o número de objetos de [**qualificador**](qualifier.md) na coleção.

## <a name="syntax"></a>Sintaxe


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

Número de objetos de [**qualificador**](qualifier.md) na coleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificadores**](qualifiers.md)
</dt> </dl>

 

 
