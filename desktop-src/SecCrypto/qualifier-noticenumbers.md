---
description: Recupera a coleção de números de aviso do usuário.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Propriedade Qualifier. NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751315"
---
# <a name="qualifiernoticenumbers-property"></a>Propriedade Qualifier. NoticeNumbers

\[A propriedade **NoticeNumbers** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]

A propriedade **NoticeNumbers** recupera a coleção de números de aviso do usuário. Esta propriedade pode estar vazia.

## <a name="syntax"></a>Syntax


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a>Valor da propriedade

A coleção de números de aviso do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificador**](qualifier.md)
</dt> </dl>

 

 
