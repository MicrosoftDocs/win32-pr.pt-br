---
title: Evento Player. CdromMediaChange
description: O evento CdromMediaChange ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD. | Evento Player. CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Evento CdromMediaChange do Windows Media Player
- Evento CdromMediaChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CdromMediaChange
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
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813660"
---
# <a name="playercdrommediachange-event"></a>Evento Player. CdromMediaChange

O evento **CdromMediaChange** ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD.

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

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O índice da unidade de CD corresponde ao índice de um objeto de **cdrom** na **cdromCollection**.

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto cdrom**](cdrom-object.md)
</dt> <dt>

[**Objeto cdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





