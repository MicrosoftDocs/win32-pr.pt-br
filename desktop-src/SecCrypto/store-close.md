---
description: Fecha um armazenamento de certificados aberto.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Método Store.Close
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
ms.openlocfilehash: e0310db88b29fea18756ecaf7a2dc142097c3a6e53dfff5892acdaf4030b9b00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897921"
---
# <a name="storeclose-method"></a>Método Store.Close

\[O **método Close** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a Classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método Close** fecha um armazenamento de [*certificados aberto.*](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintaxe


```VB
Store.Close()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Depois que **o método** Close é chamado, o [**objeto Store**](store.md) é destruído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.1 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**Aberto**](store-open.md)
</dt> </dl>

 

 
