---
title: Media.attributeCount
description: A propriedade attributeCount recupera o número de atributos que podem ser consultados e/ou definidos para o item de mídia.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media.attributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d02e120570140aa7c39a4acc7ce0eb096fffd7bccfc51a6c82d53a7ab5f3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934337"
---
# <a name="mediaattributecount"></a>Media.attributeCount

A **propriedade attributeCount** recupera o número de atributos que podem ser consultados e/ou definidos para o item de mídia.

## <a name="syntax"></a>Syntax

*player*. *currentMedia*. **attributeCount**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a Referência de Windows Media Player [atributo .](attribute-reference.md)

**Windows Media Player 10 Mobile:** Os atributos de um item de mídia estão disponíveis somente durante a reprodução, a menos que sejam recuperados do item por meio da coleção de mídias.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Mídia*. **attributeCount** para determinar o número de atributos disponíveis no item de mídia atual. O código usa esse valor para imprimir uma lista de nomes e valores de atributo em uma área de texto HTML, chamada myText. O **objeto** Player foi criado com ID = "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





