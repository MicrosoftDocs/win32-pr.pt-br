---
description: Exclui o repositório de certificados que é representado pelo objeto de armazenamento atual.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Método Store. Delete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752125"
---
# <a name="storedelete-method"></a>Método Store. Delete

\[O método **delete** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **delete** exclui o [*repositório de certificados*](../secgloss/c-gly.md) que é representado pelo objeto de [**armazenamento**](certificate.md) atual. Esse método exclui somente os repositórios que não são do sistema.

## <a name="syntax"></a>Sintaxe


```VB
Store.Delete()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os repositórios a seguir são repositórios do sistema e não podem ser excluídos:

-   Meu
-   Root
-   Confiar
-   AC
-   UserDS
-   TrustedPublisher
-   Não permitido
-   AuthRoot
-   TrustedPeople

O método **delete** retornará um erro se for chamado a partir de um script da Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Repositório**](store.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
