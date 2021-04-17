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
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769276"
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

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Esse método exclui o contêiner de chave privada referenciado pelo objeto [**PrivateKey**](privatekey.md) , bem como todas as chaves privadas no contêiner. Qualquer coisa criptografada usando as chaves públicas correspondentes às chaves privadas excluídas não poderá mais ser descriptografada.

 

Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
