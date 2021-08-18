---
title: Evento Player. MediaCollectionAttributeStringAdded
description: O evento MediaCollectionAttributeStringAdded ocorre quando um valor de atributo é adicionado à biblioteca. | Evento Player. MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Windows Media Player de eventos MediaCollectionAttributeStringAdded
- Windows Media Player de eventos MediaCollectionAttributeStringAdded, classe Player
- classe de jogador Windows Media Player, evento MediaCollectionAttributeStringAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d01bd86cb3004cb3f481222f392ba47bd1c47373f55c37ee8f0e7ded57a3d268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995866"
---
# <a name="playermediacollectionattributestringadded-event"></a>Evento Player. MediaCollectionAttributeStringAdded

O evento **MediaCollectionAttributeStringAdded** ocorre quando um valor de atributo é adicionado à biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do atributo. para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a [referência de atributo](attribute-reference.md)Windows Media Player.

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Cadeia de caracteres** que especifica o valor do atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um item de mídia é adicionado à biblioteca, seus metadados são adicionados ao objeto **mediacollection** e esse evento é acionado para cada atributo adicionado.

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Player. mediacollection**](player-mediacollection.md)
</dt> </dl>

 

 





