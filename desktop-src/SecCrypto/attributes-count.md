---
description: Recupera o número de objetos de atributo na coleção.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Propriedade Attributes. Count
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
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749462"
---
# <a name="attributescount-property"></a>Propriedade Attributes. Count

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]

A propriedade **Count** recupera o número de objetos de [**atributo**](attribute.md) na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de objetos de [**atributo**](attribute.md) na coleção. Cada objeto de **atributo** representa um único atributo na coleção.

## <a name="remarks"></a>Comentários

A propriedade **Count** pode ser usada para especificar o último objeto de [**atributo**](attribute.md) na coleção ao recuperar um objeto de **atributo** específico usando a propriedade [**Attributes. Item**](attributes-item.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 
