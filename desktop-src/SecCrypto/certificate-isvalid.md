---
description: Cria uma cadeia de verificação de certificado para um certificado e retorna um objeto CertificateStatus que contém o status de validade do certificado.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: Método ICertificate2::IsValid
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97e31129497759fa73abb4456ea8d1b8d20748bef76629d6dd857954863f5aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126976"
---
# <a name="icertificate2isvalid-method"></a>Método ICertificate2::IsValid

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método IsValid** cria uma cadeia de verificação de certificado para um certificado e retorna um objeto [**CertificateStatus**](certificatestatus.md) que contém o status de validade do certificado.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.IsValid()
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

[Objetos de criptografia](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
