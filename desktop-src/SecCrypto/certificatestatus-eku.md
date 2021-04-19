---
description: Retorna o objeto EKU usado para criar o objeto de cadeia.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Método CertificateStatus. EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770251"
---
# <a name="certificatestatuseku-method"></a>Método CertificateStatus. EKU

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **EKU** retorna o objeto [**EKU**](eku.md) usado para criar o objeto de [**cadeia**](chain.md) .

## <a name="syntax"></a>Sintaxe


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto [**EKU**](eku.md) que indica a configuração de uso estendido de chave do [*certificado*](../secgloss/c-gly.md). A configuração EKU estabelece o uso válido de um certificado. Apenas um único objeto **EKU** pode ser definido para cada certificado.

## <a name="remarks"></a>Comentários

O método [**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md) fornece a mesma funcionalidade que esse método, mas permite que muitas configurações sejam especificadas em vez de apenas um. Se a coleção de [**OIDs**](oids.md) retornada pelo método **ApplicationPolicies** contiver um ou mais objetos [**OID**](oid.md) , o objeto [**EKU**](eku.md) retornado por esse método será ignorado. Use o método **ApplicationPolicies** em vez desse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CertificateStatus**](certificatestatus.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 
