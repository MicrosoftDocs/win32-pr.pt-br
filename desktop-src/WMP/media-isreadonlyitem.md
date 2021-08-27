---
title: Método Media.isReadOnlyItem
description: O método isReadOnlyItem retorna um valor que indica se o atributo especificado do item de mídia pode ser editado.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- Método isReadOnlyItem Windows Media Player
- Método isReadOnlyItem Windows Media Player , classe media
- Classe de Windows Media Player , método isReadOnlyItem
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
ms.openlocfilehash: 501aacb7b9a56fd9780aba75a15aa9f717640ebff7619df020bad432cdffd459
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123386"
---
# <a name="mediaisreadonlyitem-method"></a>Método Media.isReadOnlyItem

O **método isReadOnlyItem** retorna um valor que indica se o atributo especificado do item de mídia pode ser editado.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que indica o nome do atributo a ser testado. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a referência Windows Media Player [atributo](attribute-reference.md)..

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **booliana.**

## <a name="remarks"></a>Comentários

Se um atributo for somente leitura, ele não poderá ser definido com o **método setItemInfo.** Observe que esse método pode retornar valores diferentes para um atributo específico quando usado com versões diferentes de Windows Media Player.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna **true.**

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Mídia*. **isReadOnlyItem para** preencher um elemento HTML TEXTAREA chamado rwText com informações sobre o item de mídia atual. O código saídas de cada atributo do item de mídia atual, juntamente com o texto que indica se o atributo é somente leitura ou leitura/gravação. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





