---
title: Método MediaCollection.getByAttribute
description: O método getByAttribute recupera uma playlist de itens de mídia que contêm um valor especificado para um atributo especificado.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- Método getByAttribute Windows Media Player
- Método getByAttribute Windows Media Player classe , MediaCollection
- Classe MediaCollection Windows Media Player método , getByAttribute
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
ms.openlocfilehash: f942f0718202d6c3e509b177c34c4c4be20c058b1e74991fa0ae89955d7711d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996305"
---
# <a name="mediacollectiongetbyattribute-method"></a>Método MediaCollection.getByAttribute

O **método getByAttribute** recupera uma playlist de itens de mídia que contêm um valor especificado para um atributo especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que indica o nome do atributo a ser pesquisado. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a Referência Windows Media Player [atributo de referência.](attribute-reference.md)

</dd> <dt>

*value* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que indica o valor que o atributo deve ter.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto Playlist.**

## <a name="remarks"></a>Comentários

Esse método pode ser usado para criar uma consulta genérica para itens de mídia que corresponderem a um valor para um atributo no banco de dados. Isso é útil no caso de atributos definidos pelo usuário. Se o atributo não existir, ocorrerá um erro.

Você pode usar esse método para recuperar todos os itens de mídia de um tipo específico. Use o nome do atributo "MediaType" e um dos seguintes valores:



| Valor    | Descrição                                                |
|----------|------------------------------------------------------------|
| áudio    | Música e outros itens somente áudio.                          |
| playlist | Listas de reprodução representadas como **objetos de** mídia.                |
| radio    | Itens da estação de rádio. Não usado pelo Windows Media Player 10.  |
| video    | Itens de vídeo.                                               |
| foto    | Itens de foto. Requer Windows Media Player 10.             |
| outros    | Outros itens, como arquivos ASF ou URLs para mídia de streaming. |



 

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir *usa MediaCollection*. **getByAttribute para** reproduzir todo o conteúdo da biblioteca pelo artista chamadoLpde 48. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





