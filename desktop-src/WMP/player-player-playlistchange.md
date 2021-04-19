---
title: Evento Player. PlaylistChange
description: O evento PlaylistChange ocorre quando uma lista de reprodução é alterada. | Evento Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Evento PlaylistChange do Windows Media Player
- Evento PlaylistChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796192"
---
# <a name="playerplaylistchange-event"></a>Evento Player. PlaylistChange

O evento **PlaylistChange** ocorre quando uma lista de reprodução é alterada.

## <a name="syntax"></a>Sintaxe


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*7.1* 
</dt> <dd>

Objeto **playlist** que foi alterado.

</dd> <dt>

*change* 
</dt> <dd>

**Número** (**longo**) indicando o tipo de alteração ocorrida na lista de reprodução. Contém um dos seguintes valores.



| Número | Nome          |
|--------|---------------|
| 0      | Unknown       |
| 1      | Limpar         |
| 2      | InfoChange    |
| 3      | Mover          |
| 4      | Excluir        |
| 5      | Inserir        |
| 6      | Acrescentar        |
| 7      | Sem suporte |
| 8      | NameChange    |
| 9      | Sem suporte |
| 10     | Sort          |



 

A constante de enumeração de estilo C pode ser derivada por meio da prefixação do valor de nome com "wmplc". Por exemplo, a constante para o estado de movimentação é **wmplcMove**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





