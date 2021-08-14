---
description: Retorna um objeto KeyUsage que indica o uso de chave válido do certificado.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: 'Método ICertificate2:: KeyUsage'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7ce3fc7246a7962ea852167cdc93e25e4d8ab11976eb3cf2868642bb906c41fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771523"
---
# <a name="icertificate2keyusage-method"></a>Método ICertificate2:: KeyUsage

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **KeyUsage** retorna um objeto [**KeyUsage**](keyusage.md) que indica o uso de chave válido do certificado.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
