---
title: Network.bandWidth
description: A propriedade bandWidth recupera a largura de banda atual do clipe.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Network.bandWidth Windows Media Player
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
ms.openlocfilehash: 40bd97ae2efe7513bc69d308a29356cfc7b141ecc84b816bdc7fad68d79aa785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616873"
---
# <a name="networkbandwidth"></a>Network.bandWidth

A **propriedade bandWidth** recupera a largura de banda atual do clipe.

## <a name="syntax"></a>Syntax

*player*. *network*. **bandWidth**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="remarks"></a>Comentários

Essa propriedade retornará zero se o *Player*. **A propriedade URL** não está definida. Essa propriedade só é válida para mídia de streaming.

## <a name="examples"></a>Exemplos

O exemplo de JScript Microsoft a seguir usa *Rede*. **bandWidth para** exibir a largura de banda de mídia atual. As informações são exibidas em um HTML DIV criado com ID = "BW". O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





