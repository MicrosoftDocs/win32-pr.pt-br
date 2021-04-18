---
title: Método mediacollection. getByAttribute
description: O método getByAttribute recupera uma lista de reprodução de itens de mídia que contêm um valor especificado para um atributo especificado.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- método getByAttribute Windows Media Player
- método getByAttribute Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByAttribute
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796408"
---
# <a name="mediacollectiongetbyattribute-method"></a>Método mediacollection. getByAttribute

O método **getByAttribute** recupera uma lista de reprodução de itens de mídia que contêm um valor especificado para um atributo especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que indica o nome do atributo a ser pesquisado. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.

</dd> <dt>

*valor* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que indica o valor que o atributo deve ter.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Esse método pode ser usado para criar uma consulta genérica para itens de mídia que correspondem a um valor para um atributo no banco de dados. Isso é útil no caso de atributos definidos pelo usuário. Se o atributo não existir, será resultado um erro.

Você pode usar esse método para recuperar todos os itens de mídia de um tipo específico. Use o nome de atributo "MediaType" e um dos seguintes valores:



| Valor    | Descrição                                                |
|----------|------------------------------------------------------------|
| áudio    | Músicas e outros itens somente de áudio.                          |
| playlist | Listas de reprodução representadas como objetos de **mídia** .                |
| radio    | Itens da estação de rádio. Não usado pelo Windows Media Player 10.  |
| video    | Itens de vídeo.                                               |
| foto    | Itens de foto. Requer o Windows Media Player 10.             |
| outros    | Outros itens, como arquivos ASF ou URLs para streaming de mídia. |



 

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mediacollection*. **getByAttribute** para reproduzir todo o conteúdo da biblioteca pelo artista chamado Triode 48. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

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

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





