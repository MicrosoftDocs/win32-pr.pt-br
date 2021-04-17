---
title: Evento Player. StringCollectionChange
description: O evento StringCollectionChange ocorre quando uma coleção de cadeia de caracteres é alterada. | Evento Player. StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Evento StringCollectionChange do Windows Media Player
- Evento StringCollectionChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento StringCollectionChange
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790591"
---
# <a name="playerstringcollectionchange-event"></a>Evento Player. StringCollectionChange

O evento StringCollectionChange ocorre quando uma coleção de cadeia de caracteres é alterada.

## <a name="syntax"></a>Sintaxe


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdispStringCollection* 
</dt> <dd>

Objeto **StringCollection** que foi alterado.

</dd> <dt>

*change* 
</dt> <dd>

Número (longo) indicando o tipo de alteração ocorrida na coleção de cadeias de caracteres. Inclui um dos valores a seguir.



|        |                                    |
|--------|------------------------------------|
| Número | Descrição                        |
| 0      | Desconhecido. (Não é um valor válido)       |
| 1      | Um item foi inserido.              |
| 2      | A coleção de cadeia de caracteres foi alterada.     |
| 3      | Um item foi excluído.               |
| 4      | A coleção de cadeias de caracteres foi limpa. |
| 5      | As atualizações em massa estão começando.        |
| 6      | Atualizações em massa encerradas.           |



 

</dd> <dt>

*lCollectionIndex* 
</dt> <dd>

Número (longo) que contém o índice do item de coleção de cadeia de caracteres que foi alterado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





