---
description: Remove o objeto OID especificado da coleção.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: Método OIDs. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796372"
---
# <a name="oidsremove-method"></a>Método OIDs. Remove

\[O método **Remove** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Remove** remove o objeto [**OID**](oid.md) especificado da coleção.

## <a name="syntax"></a>Sintaxe


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do no\]
</dt> <dd>

Índice do objeto de [**OID**](oid.md) a ser removido. Pode ser um índice na coleção ou o valor pontilhado da OID.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
