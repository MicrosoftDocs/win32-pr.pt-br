---
description: Define ou recupera o valor do número de OID pontilhado do identificador.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OIDs. Propriedade Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769278"
---
# <a name="oidvalue-property"></a>OIDs. Propriedade Value

\[A propriedade **Value** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **Value** define ou recupera o valor do número de OID pontilhado do identificador.

## <a name="syntax"></a>Syntax


```VB
OID.Value As String
```



## <a name="property-value"></a>Valor da propriedade

O valor do número de OID pontilhado do identificador. Para obter os valores possíveis, consulte Wincrypt. h.

## <a name="remarks"></a>Comentários

Se a propriedade **Value** for definida, a propriedade [**FriendlyName**](oid-friendlyname.md) será definida como o nome de exibição correspondente. Se a propriedade **FriendlyName** for definida, a propriedade **Value** será definida como o valor pontilhado correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**OIDs**](oid.md)
</dt> </dl>

 

 
