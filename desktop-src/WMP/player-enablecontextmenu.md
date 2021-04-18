---
title: Player. enableContextMenu
description: A propriedade enableContextMenu especifica ou recupera um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Player. enableContextMenu Windows Media Player
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785004"
---
# <a name="playerenablecontextmenu"></a>Player. enableContextMenu

A propriedade **enableContextMenu** especifica ou recupera um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.

## <a name="syntax"></a>Syntax

*Player*. **enableContextMenu**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um booliano de leitura/gravação.



| Valor | Descrição                       |
|-------|-----------------------------------|
| true  | Padrão. Habilite o menu de contexto. |
| false | Não habilite o menu de contexto.   |



 

## <a name="remarks"></a>Comentários

Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a "None".

**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





