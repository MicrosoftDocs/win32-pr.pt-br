---
description: Retorna um valor booliano que indica se a chave privada pertence a um conjunto de chaves do computador.
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: Método PrivateKey. ismachinekeyset
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e7fda91354ef1f381bb9e695c82931648f400708744afbc218c6a99238376d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978172"
---
# <a name="privatekeyismachinekeyset-method"></a>Método PrivateKey. ismachinekeyset

\[O método **Ismachinekeyset** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Ismachinekeyset** retorna um valor booliano que indica se a chave privada pertence a um conjunto de chaves de computador.

## <a name="syntax"></a>Sintaxe


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se for true, a chave privada pertencerá a um conjunto de chaves de computador.

## <a name="remarks"></a>Comentários

O valor de retorno desse método é dependente do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) usado. Esse método retornará um valor confiável se um Microsoft CSP for usado. Se o CSP não for um CSP da Microsoft, o valor de retorno não poderá ser confiável para ser preciso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
