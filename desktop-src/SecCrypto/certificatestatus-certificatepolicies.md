---
description: Retorna uma coleção de OIDs que representa as políticas de certificado usadas para criar o objeto de cadeia.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: Método CertificateStatus. CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753928"
---
# <a name="certificatestatuscertificatepolicies-method"></a>Método CertificateStatus. CertificatePolicies

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **CertificatePolicies** retorna uma coleção de [**OIDs**](oids.md) que representa as políticas de certificado usadas para criar o objeto de [**cadeia**](chain.md) .

## <a name="syntax"></a>Sintaxe


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Uma coleção de [**OIDs**](oids.md) . Cada objeto de [**OID**](oid.md) na coleção representa um OID de política de certificado.

## <a name="remarks"></a>Comentários

Adicione OIDs de política de certificado à coleção para especificar as políticas de certificado que devem ser usadas para criar a cadeia de certificados confiáveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
