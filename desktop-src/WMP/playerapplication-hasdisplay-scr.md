---
title: Atributo PLAYERAPPLICATION. hasDisplay
description: O atributo hasDisplay recupera um valor que indica se o vídeo pode ser exibido por meio do controle remoto do Windows Media Player.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786143"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

O atributo **hasDisplay** recupera um valor que indica se o vídeo pode ser exibido por meio do controle remoto do Windows Media Player.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** somente leitura.



| Valor | Descrição               |
|-------|---------------------------|
| True  | O vídeo pode ser exibido.    |
| Falso | O vídeo não pode ser exibido. |



 

## <a name="remarks"></a>Comentários

Esse atributo é usado somente quando você faz a comunicação remota do controle do Windows Media Player.

Vários controles do Windows Media Player podem ser executados remotamente ao mesmo tempo, mas o vídeo só pode ser exibido em um local de cada vez, seja no modo completo do Player ou em um dos controles remotos. Use essa propriedade para determinar se o controle atual é aquele pelo qual o vídeo pode ser exibido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYERAPPLICATION**](playerapplication-element.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





