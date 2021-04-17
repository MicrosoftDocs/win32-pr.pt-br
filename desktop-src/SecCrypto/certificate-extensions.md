---
description: Retorna uma coleção das extensões associadas ao certificado.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: 'Método ICertificate2:: Extensions'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cc96dee9c33bb3f76e1fb17acb2000f9740d1b5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755053"
---
# <a name="icertificate2extensions-method"></a>Método ICertificate2:: Extensions

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Extensions** retorna uma coleção das extensões associadas ao certificado. Esse método é introduzido no CAPICOM 2,0.

## <a name="syntax"></a>Sintaxe


```VB
Certificate.Extensions()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Um objeto de [**extensões**](extensions.md) que representa todas as extensões associadas ao certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
