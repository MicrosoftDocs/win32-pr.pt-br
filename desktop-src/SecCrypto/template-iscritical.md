---
description: Recupera um valor booliano que indica se a extensão do modelo está marcada como crítica.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Propriedade modelo. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751924"
---
# <a name="templateiscritical-property"></a>Propriedade modelo. IsCritical

\[A propriedade **Iscriticad** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]

A propriedade **Iscriticat** recupera um valor booliano que indica se a extensão do modelo está marcada como crítica.

## <a name="syntax"></a>Syntax


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **for true**, a extensão do modelo será marcada como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Modelo**](template.md)
</dt> </dl>

 

 
