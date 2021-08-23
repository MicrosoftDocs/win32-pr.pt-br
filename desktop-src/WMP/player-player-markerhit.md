---
title: Evento Player.MarkerHit
description: O evento MarkerHit ocorre quando um marcador é atingido. | Evento Player.MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Evento MarkerHit Windows Media Player
- Evento MarkerHit Windows Media Player , classe Player
- Classe player Windows Media Player evento , MarkerHit
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
ms.openlocfilehash: b065b9c7499beb2433c0b7c76180a6073b13be589f710aec0810299ab249b91c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389106"
---
# <a name="playermarkerhit-event"></a>Evento Player.MarkerHit

O **evento MarkerHit** ocorre quando um marcador é atingido.

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

**Número** (**longo**) que indica o número do marcador que foi atingido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo JScript importado usando o nome do parâmetro especificado. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





