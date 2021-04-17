---
description: Recupera o número de versão secundária do modelo.
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: Propriedade Template. MinorVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a1de0beb41cbe87ca86b443c5cc2145c2058073
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749881"
---
# <a name="templateminorversion-property"></a>Propriedade Template. MinorVersion

\[A propriedade **MinorVersion** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]

A propriedade **MinorVersion** recupera o número de versão secundária do modelo.

## <a name="syntax"></a>Syntax


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de versão secundária do modelo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Modelo**](template.md)
</dt> </dl>

 

 
