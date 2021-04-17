---
title: Evento Player. MediaCollectionAttributeStringRemoved
description: O evento MediaCollectionAttributeStringRemoved ocorre quando um valor de atributo é removido da biblioteca. | Evento Player. MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Evento MediaCollectionAttributeStringRemoved do Windows Media Player
- Evento MediaCollectionAttributeStringRemoved Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaCollectionAttributeStringRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782414"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Evento Player. MediaCollectionAttributeStringRemoved

O evento **MediaCollectionAttributeStringRemoved** ocorre quando um valor de atributo é removido da biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do atributo. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Cadeia de caracteres** que especifica o valor do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um item de mídia é removido da biblioteca, seus metadados são removidos do objeto **mediacollection** e esse evento é acionado para cada atributo removido.

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

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

 

 





