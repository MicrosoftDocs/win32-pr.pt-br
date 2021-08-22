---
title: Atributo PLAYERAPPLICATION. hasDisplay
description: o atributo hasDisplay recupera um valor que indica se o vídeo pode ser exibido por meio do controle de Windows Media Player remoto.
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
ms.openlocfilehash: ac144f7e9f96db707944cbb016028578d2446be43a0f06cd0293cb5d56f84c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571939"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

o atributo **hasDisplay** recupera um valor que indica se o vídeo pode ser exibido por meio do controle de Windows Media Player remoto.

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

esse atributo é usado somente quando você faz a comunicação remota do controle de Windows Media Player.

vários controles de Windows Media Player podem ser executados remotamente ao mesmo tempo, mas o vídeo só pode ser exibido em um local por vez, seja no modo completo do Player ou em um dos controles remotos. Use essa propriedade para determinar se o controle atual é aquele pelo qual o vídeo pode ser exibido.

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

 

 





