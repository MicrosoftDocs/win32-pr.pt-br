---
description: Recupera a ID de objeto do qualificador.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Propriedade Qualifier. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42c2f83d4fa8be31991a98b6fe4cfc6a741e2190cd12d54bfd5e968951472bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901046"
---
# <a name="qualifieroid-property"></a>Propriedade Qualifier. OID

\[A propriedade **OID** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]

A propriedade **OID** recupera a ID de objeto do qualificador. Essa é a propriedade padrão.

## <a name="syntax"></a>Sintaxe


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**OID**](oid.md) que identifica o qualificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificador**](qualifier.md)
</dt> </dl>

 

 
