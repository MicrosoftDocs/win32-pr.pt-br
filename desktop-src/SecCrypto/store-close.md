---
description: Fecha um repositório de certificados aberto.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Método Store. Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756850"
---
# <a name="storeclose-method"></a>Método Store. Close

\[O método **Close** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Close** fecha um [*repositório de certificados*](../secgloss/c-gly.md)aberto.

## <a name="syntax"></a>Sintaxe


```VB
Store.Close()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Depois que o método **Close** é chamado, o objeto [**Store**](store.md) é destruído.

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
</dt> <dt>

[**Aberto**](store-open.md)
</dt> </dl>

 

 
