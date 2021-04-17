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
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762023"
---
# <a name="certificatethumbprint-property"></a>Propriedade Certificate. Thumbprint

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

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
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificate**](certificate.md)
</dt> </dl>

 

 
