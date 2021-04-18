---
title: Player. status
description: A propriedade status recupera um valor que indica o status do Windows Media Player.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player. status Windows Media Player
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814020"
---
# <a name="playerstatus"></a>Player. status

A propriedade **status** recupera um valor que indica o status do Windows Media Player.

## <a name="syntax"></a>Syntax

*Player* . **status** do

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma cadeia de caracteres somente leitura.

## <a name="remarks"></a>Comentários

Os valores contidos nessa propriedade estão sujeitos a alterações a qualquer momento e devem ser usados apenas para fins de exibição.

O evento **StatusChange** é acionado sempre que essa propriedade altera o valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 7,0 ou posterior.<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Evento Player. StatusChange**](player-player-statuschange.md)
</dt> </dl>

 

 





