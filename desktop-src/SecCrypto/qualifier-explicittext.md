---
description: Recupera o conteúdo do aviso do usuário.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Propriedade Qualifier. ExplicitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 60753e0e7fa9996f9584070d6fac2d12d3a483b681fa61b72cf2e59cc2898995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901107"
---
# <a name="qualifierexplicittext-property"></a>Propriedade Qualifier. ExplicitText

\[A propriedade **ExplicitText** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]

A propriedade **ExplicitText** recupera o conteúdo do aviso do usuário. Esta propriedade pode estar vazia.

## <a name="syntax"></a>Syntax


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a>Valor da propriedade

O conteúdo do aviso do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificador**](qualifier.md)
</dt> </dl>

 

 
