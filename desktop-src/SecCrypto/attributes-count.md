---
description: Recupera o número de objetos Attribute na coleção.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Propriedade Attributes.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d7b1f2213fc6de3ec08a9c9b568222f5dd54a6de6f9bdb3adb27e052e8c088e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773501"
---
# <a name="attributescount-property"></a>Propriedade Attributes.Count

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use [**a Classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System.Security.Cryptography.**](/previous-versions/windows/)\]

A **propriedade Count** recupera o número de objetos [**Attribute**](attribute.md) na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de [**objetos Attribute**](attribute.md) na coleção. Cada **objeto** Attribute representa um único atributo na coleção.

## <a name="remarks"></a>Comentários

A **propriedade Count** pode ser usada para especificar o último objeto [**Attribute**](attribute.md) na coleção ao recuperar um objeto **Attribute** específico usando a [**propriedade Attributes.Item.**](attributes-item.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 
