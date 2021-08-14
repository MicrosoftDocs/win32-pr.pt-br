---
description: Determina se o certificado tem uma chave privada associada a ele. O método determina isso verificando se a propriedade CERT \_ KEY \_ PROV \_ INFO PROP \_ \_ ID está presente.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: Método ICertificate2::HasPrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ac38a62e11d75e21de5fd61dffd821cb4384e4e9b59d2bf11f6e217589ab578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771521"
---
# <a name="icertificate2hasprivatekey-method"></a>Método ICertificate2::HasPrivateKey

\[CAPICOM é um componente de apenas 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método HasPrivateKey** determina se [*o*](../secgloss/c-gly.md) certificado tem uma [*chave privada*](../secgloss/p-gly.md) associada a ele. O método determina isso verificando se a propriedade CERT \_ KEY \_ PROV \_ INFO PROP \_ \_ ID está presente.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PrivateKey.Open**](privatekey-open.md)
</dt> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
