---
description: Retorna uma coleção de OIDs que representa as políticas de aplicativo usadas para criar o objeto de cadeia.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: Método CertificateStatus. ApplicationPolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a27bc08f658e317b41380b2dabd9aadc13e8b50bd4985c0fd13211fa81fd507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770433"
---
# <a name="certificatestatusapplicationpolicies-method"></a>Método CertificateStatus. ApplicationPolicies

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **ApplicationPolicies** retorna uma coleção de [**OIDs**](oids.md) que representa as políticas de aplicativo usadas para criar o objeto de [**cadeia**](chain.md) .

## <a name="syntax"></a>Sintaxe


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Uma coleção de [**OIDs**](oids.md) . Cada objeto de [**OID**](oid.md) na coleção representa um OID de política de aplicativo.

## <a name="remarks"></a>Comentários

Adicione OIDs de política de aplicativo à coleção para especificar as políticas de aplicativo que devem ser usadas para criar a cadeia de certificados confiáveis. Se a coleção contiver pelo menos um objeto [**OID**](oid.md) , o objeto [**EKU**](eku.md) retornado pelo método [**CertificateStatus. EKU**](certificatestatus-eku.md) será ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
