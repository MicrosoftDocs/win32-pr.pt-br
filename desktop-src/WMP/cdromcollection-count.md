---
title: CdromCollection.count
description: A propriedade count recupera o número de unidades de CD e DVD disponíveis no sistema.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection.count Windows Media Player
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
ms.openlocfilehash: 0db279f746640d09fac8b3852773afc27330fc9ca48d59a1470de7d42709e60f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864096"
---
# <a name="cdromcollectioncount"></a>CdromCollection.count

A **propriedade count** recupera o número de unidades de CD e DVD disponíveis no sistema.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

As unidades de DVD-ROM são contadas exatamente como unidades de CD. No entanto, o Windows Media Player somente dá suporte à funcionalidade de DVD para Windows XP ou sistemas operacionais posteriores. Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídia de DVD.

**Windows Media Player 10 Mobile:** Esse método sempre retorna 0.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir *usa CdromCollection*. **contagem** para exibir o número de unidades de CD e DVD disponíveis no computador do usuário. O objeto player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





