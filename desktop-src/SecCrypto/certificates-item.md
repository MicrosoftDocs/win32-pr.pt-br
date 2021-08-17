---
description: Recupera um objeto de certificado que representa o certificado indexado da coleção. Essa é a propriedade padrão.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Propriedade Certificates. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 927f52570b515c6699458cfb802b5c315201d401e9bcf5e0be76ab41863bd47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770535"
---
# <a name="certificatesitem-property"></a>Propriedade Certificates. Item

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Item** recupera um objeto de [**certificado**](certificate.md) que representa o certificado indexado da coleção. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valor da propriedade

Um objeto de [**certificado**](certificate.md) que representa o certificado indexado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
