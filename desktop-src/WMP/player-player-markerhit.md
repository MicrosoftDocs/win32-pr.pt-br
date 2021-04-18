---
title: Evento Player. MarkerHit
description: O evento MarkerHit ocorre quando um marcador é atingido. | Evento Player. MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Evento MarkerHit do Windows Media Player
- Evento MarkerHit Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MarkerHit
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760431"
---
# <a name="playermarkerhit-event"></a>Evento Player. MarkerHit

O evento **MarkerHit** ocorre quando um marcador é atingido.

## <a name="syntax"></a>Sintaxe


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MarkerNum* 
</dt> <dd>

**Número** (**longo**) indicando o número do marcador que foi atingido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





