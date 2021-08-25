---
description: Recupera uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Propriedade Certificate. Thumbprint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 64748f3eb8b9623ea7c07a7428f29b30276c34ab38631fdbf210b25b5be92a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878156"
---
# <a name="certificatethumbprint-property"></a>Propriedade Certificate. Thumbprint

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade de **impressão digital** recupera uma cadeia de caracteres hexadecimal que contém o hash [*SHA-1*](../secgloss/s-gly.md) do certificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
