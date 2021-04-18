---
description: Define ou recupera o nome de exibição para o identificador.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OIDs. Propriedade FriendlyName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780913"
---
# <a name="oidfriendlyname-property"></a>OIDs. Propriedade FriendlyName

\[A propriedade **FriendlyName** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **FriendlyName** define ou recupera o nome de exibição para o identificador.

## <a name="syntax"></a>Syntax


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a>Valor da propriedade

O nome de exibição para o [**OID**](oid.md).

## <a name="remarks"></a>Comentários

Se a propriedade **FriendlyName** for definida, a propriedade [**Value**](oid-value.md) será definida como o valor pontilhado correspondente. Se a propriedade **Value** for definida, a propriedade **FriendlyName** será definida como o nome de exibição correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**OIDs**](oid.md)
</dt> </dl>

 

 
