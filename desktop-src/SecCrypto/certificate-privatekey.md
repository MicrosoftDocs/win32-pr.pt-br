---
description: Define ou recupera a chave privada associada ao certificado.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Propriedade Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755315"
---
# <a name="certificateprivatekey-property"></a>Propriedade Certificate. PrivateKey

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **PrivateKey** define ou recupera a chave privada associada ao certificado. Esta propriedade foi introduzida no CAPICOM 2,0.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**PrivateKey**](privatekey.md) que representa a chave privada associada ao certificado.

## <a name="remarks"></a>Comentários

Definir a propriedade **PrivateKey** como Nothing remove a associação entre a chave privada e o certificado, mas não exclui a chave privada. Para excluir a chave privada, chame o método [**PrivateKey. Delete**](privatekey-delete.md) e, em seguida, defina essa propriedade como Nothing.

Essa propriedade gera CAPICOM \_ E \_ não \_ são permitidos quando ele é definido de um aplicativo baseado na Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
