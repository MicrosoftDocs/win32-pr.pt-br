---
title: Método mediacollection. getAttributeStringCollection
description: O método getAttributeStringCollection recupera um objeto StringCollection que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia especificado.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- Windows Media Player do método getAttributeStringCollection
- método getAttributeStringCollection Windows Media Player, classe mediacollection
- classe mediacollection Windows Media Player, método getAttributeStringCollection
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27b7c6dbef585763ecfda1abdc7beadfa3d883476033424ff868a3d56c4bb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996296"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>Método mediacollection. getAttributeStringCollection

O método **getAttributeStringCollection** recupera um objeto **StringCollection** que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o atributo.

</dd> <dt>

*MediaType* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que representa o tipo de mídia. Contém um dos seguintes valores: "áudio", "vídeo", "playlist" ou "outros".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um objeto **StringCollection** .

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a seção [referência de atributo](attribute-reference.md) .

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *mediacollection*. **getAttributeStringCollection** para exibir uma lista de valores que correspondem a um atributo específico para itens de áudio na coleção de mídia. Um elemento HTML SELECT, criado com ID = "Attribute", permite ao usuário selecionar um atributo, como artista, gênero ou álbum. Um elemento de TEXTAREA HTML, criado com ID = "AttributeVals", exibe o resultado. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





