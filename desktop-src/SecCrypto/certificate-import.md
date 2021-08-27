---
description: Importa um certificado codificado anteriormente de uma cadeia de caracteres para o objeto de certificado.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'Método ICertificate2:: Import'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1f47ebe884c8fb3a10a8ebdef89353e7549c916a7793075d0086d2f0cd2ce717
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127006"
---
# <a name="icertificate2import-method"></a>Método ICertificate2:: Import

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método de **importação** importa um certificado codificado anteriormente de uma cadeia de caracteres para o objeto de [**certificado**](certificate.md) . Chamar esse método redefine o [*estado*](../secgloss/s-gly.md) desse objeto.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncodedCertificate* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém os dados de certificado codificados a serem importados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

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

 

 
