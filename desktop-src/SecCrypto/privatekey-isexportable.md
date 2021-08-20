---
description: Retorna um valor booliana que indica se a chave privada é exportável.
ms.assetid: 56e72747-126d-4bb4-ac10-ced0acef388b
title: Método PrivateKey.IsExportable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsExportable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e4056690be8661628baa1723583489375b37cbb69d2fc9340e218ece87a314b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978422"
---
# <a name="privatekeyisexportable-method"></a>Método PrivateKey.IsExportable

\[O **método IsExportable** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a propriedade X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método IsExportable** retorna um valor booliana que indica se a chave privada é exportável.

## <a name="syntax"></a>Sintaxe


```VB
PrivateKey.IsExportable()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se true, a chave privada será marcada como exportável.

## <a name="remarks"></a>Comentários

O valor de retorno desse método depende do CSP (provedor de [*serviços*](../secgloss/c-gly.md) criptográficos) usado. Esse método retornará um valor confiável se um CSP da Microsoft for usado. Se o CSP não for um CSP da Microsoft, o valor de retorno não poderá ser confiável para ser preciso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Privatekey**](privatekey.md)
</dt> </dl>

 

 
