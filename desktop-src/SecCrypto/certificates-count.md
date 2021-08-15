---
description: Recupera o número de objetos Certificate na coleção.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Propriedade Certificates.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 703b929ee4b9cbe69a0f2ff37ad7e1d0c2c0005c0aa461fc38a14baa8a8ab443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770545"
---
# <a name="certificatescount-property"></a>Propriedade Certificates.Count

\[CAPICOM é um componente de apenas 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade Count** recupera o número de objetos [**Certificate**](certificate.md) na coleção.

## <a name="syntax"></a>Syntax


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de [**objetos certificate**](certificate.md) na coleção. Cada **objeto** Certificate representa um único certificado na coleção.

## <a name="remarks"></a>Comentários

CAPICOM dá suporte apenas a um único certificado para o [*armazenamento de cartão*](../secgloss/s-gly.md) inteligente. Mesmo que o armazenamento de cartão inteligente contenha mais de um certificado, essa propriedade conterá 1. Para obter mais informações sobre o armazenamento de cartão inteligente, consulte o membro DO ARMAZENAMENTO DE USUÁRIO DO CARTÃO **INTELIGENTE CAPICOM \_ \_ \_ \_** da enumeração [**CAPICOM \_ STORE \_ LOCATION.**](capicom-store-location.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
