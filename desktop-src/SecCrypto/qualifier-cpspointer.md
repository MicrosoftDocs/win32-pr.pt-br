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
ms.openlocfilehash: b7e24cd47c26c2ec365fc8c52be7319b325199fdfca8af2a0f9967a9713a9c81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975840"
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
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificador**](qualifier.md)
</dt> </dl>

 

 
