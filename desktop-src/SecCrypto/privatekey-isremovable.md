---
description: Retorna um valor booliano que indica se a chave privada está no armazenamento removível.
ms.assetid: 9371d7cf-65b2-4c0f-a387-195a058d6a8b
title: Método PrivateKey. IsRemovable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsRemovable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6684d40302746a736701b824685a54faeff5354a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770450"
---
# <a name="privatekeyisremovable-method"></a>Método PrivateKey. IsRemovable

\[O método **IsRemovable** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **IsRemovable** retorna um valor booliano que indica se a chave privada está no armazenamento removível.

## <a name="syntax"></a>Sintaxe


```VB
PrivateKey.IsRemovable()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se for true, a chave privada estará no armazenamento removível.

## <a name="remarks"></a>Comentários

O valor de retorno desse método é dependente do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) usado. Esse método retornará um valor confiável se um Microsoft CSP for usado. Se o CSP não for um CSP da Microsoft, o valor de retorno não poderá ser confiável para ser preciso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
