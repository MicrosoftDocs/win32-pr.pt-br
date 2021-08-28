---
description: Adiciona um objeto de certificado à coleção.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'Método ICertificates2:: Add'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4de1c00e3f006a69fa3c6babfa2aa44a1ad618050e5802ac4c9578dc3f93937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101046"
---
# <a name="icertificates2add-method"></a>Método ICertificates2:: Add

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Add** adiciona um objeto de [**certificado**](certificate.md) à coleção. Esse método é introduzido no CAPICOM 2,0.

## <a name="syntax"></a>Sintaxe


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Certificado* \[ do no\]
</dt> <dd>

O objeto de [**certificado**](certificate.md) a ser adicionado à coleção.

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



 

 
