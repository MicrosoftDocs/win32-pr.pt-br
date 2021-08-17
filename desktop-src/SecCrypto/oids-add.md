---
description: Adiciona o objeto OID especificado à coleção.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Método OIDs. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff686ae816fa61d68e0a0c40326581025ced8f4c94fb5cffc633ff452ac4f0ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979647"
---
# <a name="oidsadd-method"></a>Método OIDs. Add

\[O método **Add** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Add** adiciona o objeto [**OID**](oid.md) especificado à coleção.

## <a name="syntax"></a>Sintaxe


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OID* \[ no\]
</dt> <dd>

O objeto de [**OID**](oid.md) a ser adicionado à coleção. O objeto **OID** é adicionado na ordem classificada com base em seu valor pontilhado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
