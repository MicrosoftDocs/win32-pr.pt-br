---
title: Evento Player. PlaylistChange
description: O evento PlaylistChange ocorre quando uma lista de reprodução é alterada. | Evento Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Windows Media Player de eventos PlaylistChange
- Windows Media Player de eventos PlaylistChange, classe Player
- classe de jogador Windows Media Player, evento PlaylistChange
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
ms.openlocfilehash: 3ff4c45449c8de2062aa53ce9bda89c8d634dd30bc1ac8c03f091e8b97e9ce60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572799"
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

*Playlist* 
</dt> <dd>

Objeto **playlist** que foi alterado.

</dd> <dt>

*change* 
</dt> <dd>

**Número** (**longo**) indicando o tipo de alteração ocorrida na lista de reprodução. Contém um dos seguintes valores.



| Número | Name          |
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

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

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

 

 





