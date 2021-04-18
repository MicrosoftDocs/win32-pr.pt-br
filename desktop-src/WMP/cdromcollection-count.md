---
title: CdromCollection. contagem
description: A propriedade Count recupera o número de unidades de CD e DVD disponíveis no sistema.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection. contagem do Windows Media Player
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760275"
---
# <a name="cdromcollectioncount"></a>CdromCollection. contagem

A propriedade **Count** recupera o número de unidades de CD e DVD disponíveis no sistema.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

As unidades de DVD-ROM são contadas exatamente como unidades de CD. No entanto, o controle do Windows Media Player só dá suporte à funcionalidade de DVD para sistemas operacionais Windows XP ou posteriores. Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídias em DVD.

**Windows Media Player 10 Mobile:** Esse método sempre retorna 0.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *cdromCollection*. **contagem** para exibir o número de unidades de CD e DVD disponíveis no computador do usuário. O objeto de jogador foi criado com ID = "Player".


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto cdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





