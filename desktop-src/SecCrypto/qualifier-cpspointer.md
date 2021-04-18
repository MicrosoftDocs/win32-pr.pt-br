---
description: Recupera o URI que aponta para uma declaração de prática de certificação (CPS) publicada pela autoridade de certificação (CA).
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Propriedade Qualifier. CPSPointer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750092"
---
# <a name="qualifiercpspointer-property"></a>Propriedade Qualifier. CPSPointer

\[A propriedade **CPSPointer** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]

A propriedade **CPSPointer** recupera o URI que aponta para uma declaração de prática de certificação (CPS) publicada pela autoridade de certificação (CA).

## <a name="syntax"></a>Syntax


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a>Valor da propriedade

O URI que aponta para um CPS publicado pela autoridade de certificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificador**](qualifier.md)
</dt> </dl>

 

 
