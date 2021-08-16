---
title: Evento Player.CdromMediaChange
description: O evento CdromMediaChange ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD. | Evento Player.CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Evento CdromMediaChange Windows Media Player
- Evento CdromMediaChange Windows Media Player , classe Player
- Classe player Windows Media Player , evento CdromMediaChange
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5e7301c1fb697f4dbbceea2d4dc46af1d884fe4b3e06166b5c24aa43502a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747382"
---
# <a name="playercdrommediachange-event"></a>Evento Player.CdromMediaChange

O **evento CdromMediaChange** ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD.

## <a name="syntax"></a>Sintaxe


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CdromNum* 
</dt> <dd>

**Número** (**longo**) especificando o índice da unidade de CD ou DVD.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O índice da unidade de CD corresponde ao índice de um **objeto Cdrom** na **CdromCollection.**

O valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo JScript importado usando o nome do parâmetro especificado. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Cdrom**](cdrom-object.md)
</dt> <dt>

[**Objeto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





