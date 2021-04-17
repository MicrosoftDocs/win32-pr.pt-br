---
title: Rede. largura de banda
description: A propriedade bandWidth recupera a largura de banda atual do clipe.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Rede. largura de banda Windows Media Player
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772937"
---
# <a name="networkbandwidth"></a>Rede. largura de banda

A propriedade **Bandwidth** recupera a largura de banda atual do clipe.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **largura de banda**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Essa propriedade retornará zero se o *Player*. A propriedade da **URL** não está definida. Esta propriedade só é válida para mídia de streaming.

## <a name="examples"></a>Exemplos

O exemplo do Microsoft JScript a seguir usa a *rede*. **largura de banda** para exibir a largura de banda de mídia atual. As informações são exibidas em uma DIV HTML criada com ID = "BW". O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





