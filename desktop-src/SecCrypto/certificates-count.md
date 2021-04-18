---
description: Recupera o número de objetos de certificado na coleção.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Propriedade Certificates. Count
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
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760392"
---
# <a name="certificatescount-property"></a>Propriedade Certificates. Count

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Count** recupera o número de objetos de [**certificado**](certificate.md) na coleção.

## <a name="syntax"></a>Syntax


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de objetos de [**certificado**](certificate.md) na coleção. Cada objeto de **certificado** representa um único certificado na coleção.

## <a name="remarks"></a>Comentários

O capicor dá suporte apenas a um único certificado para o repositório de [*cartão inteligente*](../secgloss/s-gly.md) . Mesmo que o armazenamento de cartão inteligente contenha mais de um certificado, essa propriedade conterá 1. Para obter mais informações sobre o repositório de cartão inteligente, consulte o membro do **\_ repositório de \_ \_ usuários \_ do cartão inteligente CAPICOM** da enumeração do [**\_ \_ local de armazenamento CAPICOM**](capicom-store-location.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificados**](certificates.md)
</dt> </dl>

 

 
