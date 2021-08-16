---
title: Evento Player. MediaCollectionAttributeStringChanged
description: O evento MediaCollectionAttributeStringChanged ocorre quando um valor de atributo na biblioteca é alterado. | Evento Player. MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Windows Media Player de eventos MediaCollectionAttributeStringChanged
- Windows Media Player de eventos MediaCollectionAttributeStringChanged, classe Player
- classe de jogador Windows Media Player, evento MediaCollectionAttributeStringChanged
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9435be90761abf88927789fad4380172f0ef6f31427848195d3aa14ea4112cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747392"
---
# <a name="playermediacollectionattributestringchanged-event"></a>Evento Player. MediaCollectionAttributeStringChanged

O evento **MediaCollectionAttributeStringChanged** ocorre quando um valor de atributo na biblioteca é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do atributo. para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a [referência de atributo](attribute-reference.md)Windows Media Player.

</dd> <dt>

*bstrOldAttribVal* 
</dt> <dd>

**Cadeia de caracteres** que especifica o valor antigo do atributo.

</dd> <dt>

*bstrNewAttribVal* 
</dt> <dd>

**Cadeia de caracteres** que especifica o novo valor do atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um usuário modifica os metadados da biblioteca, o objeto **mediacollection** é atualizado e esse evento é acionado para cada atributo alterado.

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Player. mediacollection**](player-mediacollection.md)
</dt> </dl>

 

 





