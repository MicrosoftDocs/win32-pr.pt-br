---
title: Método Media. setItemInfo
description: O método setItemInfo define o valor do atributo especificado para o item de mídia atual.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Windows Media Player do método setItemInfo
- método setItemInfo Windows Media Player, classe Media
- classe de mídia Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1639b86ce1e0643f3d6ce255e5ca492bc4fae0c1301e1a568a0c5609ceda2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647966"
---
# <a name="mediasetiteminfo-method"></a>Método Media. setItemInfo

O método **setItemInfo** define o valor do atributo especificado para o item de mídia atual.

## <a name="syntax"></a>Sintaxe


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo. para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a [referência de atributo](attribute-reference.md)Windows Media Player.

</dd> <dt>

*valor* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o novo valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A propriedade **attributeCount** contém o número de atributos disponíveis para um determinado objeto de **mídia** . Os números de índice podem ser usados com o método **GetAttributeName** para determinar os nomes dos atributos internos que podem ser usados com esse método.

Antes de usar esse método, use o método **isReadOnlyItem** para determinar se um atributo específico pode ser definido.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Observação**

se você inserir o controle de Windows Media Player em seu aplicativo, os atributos de arquivo que você alterar não serão gravados no arquivo de mídia digital até que o usuário seja executado Windows Media Player. Se você usar o controle em um aplicativo remoto escrito em C++, os atributos de arquivo alterados serão gravados no arquivo de mídia digital logo depois que você fizer as alterações. Em ambos os casos, as alterações ficam imediatamente disponíveis para seu código por meio da biblioteca.

**Windows Media Player 10 Mobile:** Este método não está implementado.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *mídia*. **setItemInfo** para alterar o valor do atributo gênero para o item de mídia atual. Um elemento de entrada de texto HTML chamado genText permite que o usuário insira uma cadeia de texto, que é usada para alterar as informações de atributo. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

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

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. isReadOnlyItem**](media-isreadonlyitem.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





