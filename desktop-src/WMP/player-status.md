---
title: Player. status
description: A propriedade status recupera um valor que indica o status de Windows Media Player.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Windows Media Player Player. status
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
ms.openlocfilehash: a03ef010bfcb5ee936183724331e97fac5d6f5912d87c5281a55106519c104e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572045"
---
# <a name="playerstatus"></a>Player. status

A propriedade **status** recupera um valor que indica o status de Windows Media Player.

## <a name="syntax"></a>Sintaxe

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

 

 





