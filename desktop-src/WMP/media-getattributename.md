---
title: Método Media. GetAttributeName
description: O método GetAttributeName recupera o nome do atributo correspondente ao índice especificado.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- método GetAttributeName Windows Media Player
- método getattributename Windows Media Player, classe de mídia
- classe de mídia Windows Media Player, método getattributename
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b9a288830283b3711c6e4eb652be968979628af48d2ce5b718150b9018568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123426"
---
# <a name="mediagetattributename-method"></a>Método Media. GetAttributeName

O método **GetAttributeName** recupera o nome do atributo correspondente ao índice especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que contém o índice do atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna uma **cadeia de caracteres** especificando o nome do atributo.

## <a name="remarks"></a>Comentários

O nome do atributo retornado pode ser usado em conjunto com **getItemInfo** para recuperar o valor de um atributo nomeado específico.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a [referência de atributo](attribute-reference.md)de Windows Media Player..

**Windows Media Player 10 Mobile:** Os atributos de um item de mídia estão disponíveis somente durante a reprodução, a menos que sejam recuperados do item por meio da coleção de mídia.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *mídia*. **GetAttributeName** para preencher uma área de texto HTML chamada MyText com o índice e o nome de cada atributo para o item de mídia atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
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

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





