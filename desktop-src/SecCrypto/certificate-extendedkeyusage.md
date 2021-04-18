---
description: Retorna um objeto ExtendedKeyUsage que indica os usos válidos do certificado.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: 'Método ICertificate2:: ExtendedKeyUsage'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754952"
---
# <a name="icertificate2extendedkeyusage-method"></a>Método ICertificate2:: ExtendedKeyUsage

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **ExtendedKeyUsage** retorna um objeto [**ExtendedKeyUsage**](extendedkeyusage.md) que indica os usos válidos do certificado.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

O objeto [**ExtendedKeyUsage**](extendedkeyusage.md) que está associado ao certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
