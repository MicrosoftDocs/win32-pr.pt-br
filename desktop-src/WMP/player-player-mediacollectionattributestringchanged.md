---
title: Evento Player. MediaCollectionAttributeStringChanged
description: O evento MediaCollectionAttributeStringChanged ocorre quando um valor de atributo na biblioteca é alterado. | Evento Player. MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Evento MediaCollectionAttributeStringChanged do Windows Media Player
- Evento MediaCollectionAttributeStringChanged Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaCollectionAttributeStringChanged
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
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814024"
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

**Cadeia de caracteres** que especifica o nome do atributo. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.

</dd> <dt>

*bstrOldAttribVal* 
</dt> <dd>

**Cadeia de caracteres** que especifica o valor antigo do atributo.

</dd> <dt>

*bstrNewAttribVal* 
</dt> <dd>

**Cadeia de caracteres** que especifica o novo valor do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um usuário modifica os metadados da biblioteca, o objeto **mediacollection** é atualizado e esse evento é acionado para cada atributo alterado.

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

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

 

 





