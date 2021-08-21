---
description: Exclui o contêiner de chave privada referenciado pelo objeto PrivateKey.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: Método PrivateKey. Delete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e9eb69223eeabae3ca1803869bf887d66e77a4f2466f35bedbf87435839ee73f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978442"
---
# <a name="privatekeydelete-method"></a>Método PrivateKey. Delete

\[O método **delete** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **delete** exclui o contêiner de chave privada referenciado pelo objeto [**PrivateKey**](privatekey.md) .

## <a name="syntax"></a>Sintaxe


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Esse método exclui o contêiner de chave privada referenciado pelo objeto [**PrivateKey**](privatekey.md) , bem como todas as chaves privadas no contêiner. Qualquer coisa criptografada usando as chaves públicas correspondentes às chaves privadas excluídas não poderá mais ser descriptografada.

 

Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
