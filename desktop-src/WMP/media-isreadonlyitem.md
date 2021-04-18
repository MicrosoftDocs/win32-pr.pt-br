---
title: Método Media. isReadOnlyItem
description: O método isReadOnlyItem retorna um valor que indica se o atributo especificado do item de mídia pode ser editado.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- método isReadOnlyItem Windows Media Player
- método isReadOnlyItem Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método isReadOnlyItem
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788888"
---
# <a name="mediaisreadonlyitem-method"></a>Método Media. isReadOnlyItem

O método **isReadOnlyItem** retorna um valor que indica se o atributo especificado do item de mídia pode ser editado.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que indica o nome do atributo a ser testado. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player..

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **valor booleano**.

## <a name="remarks"></a>Comentários

Se um atributo for somente leitura, ele não poderá ser definido com o método **setItemInfo** . Observe que esse método pode retornar valores diferentes para um atributo específico quando usado com versões diferentes do Windows Media Player.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna **true**.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mídia*. **isReadOnlyItem** para preencher um elemento de TextArea HTML chamado rwText com informações sobre o item de mídia atual. O código gera cada atributo do item de mídia atual, juntamente com o texto que indica se o atributo é somente leitura ou leitura/gravação. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





