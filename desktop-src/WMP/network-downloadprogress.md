---
title: Network.downloadProgress
description: A propriedade downloadProgress recupera o percentual de download concluído.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Network.downloadProgress Windows Media Player
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc8d2707cd5fc24129363d53f9ee58fedf7b15c5da4eb5b80f032524ee66c09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901716"
---
# <a name="networkdownloadprogress"></a>Network.downloadProgress

A **propriedade downloadProgress** recupera o percentual de download concluído.

## <a name="syntax"></a>Syntax

*player*. *network*. **downloadProgress**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="remarks"></a>Comentários

Quando o controle Windows Media Player está conectado a um arquivo de mídia que pode ser reproduzido e baixado ao mesmo tempo, a propriedade **downloadProgress** retorna a porcentagem do arquivo total que foi baixado. Atualmente, esse recurso tem suporte apenas em servidores Web. Os seguintes formatos de arquivo podem ser baixados e tocados simultaneamente:

-   Advanced Systems Format (ASF)
-   Áudio do Windows Media (WMA)
-   Vídeo do Windows Media (WMV)
-   MP3
-   Mpeg
-   WAV
-   Alguns arquivos AVI

Use o *Player*. **Evento de buffer** para determinar quando o download começa e termina.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Rede*. **downloadProgress para** exibir o percentual de download concluído. As informações são exibidas em um HTML DIV criado com ID = "DP". O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O **objeto** Player foi criado com ID = "Player".


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
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

[**Evento Player.Buffering**](player-player-buffering.md)
</dt> </dl>

 

 





