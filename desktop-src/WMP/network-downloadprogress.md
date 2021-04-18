---
title: Network. downloadProgress
description: A propriedade downloadProgress recupera a porcentagem de download concluído.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Network. downloadProgress Windows Media Player
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
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781258"
---
# <a name="networkdownloadprogress"></a>Network. downloadProgress

A propriedade **downloadProgress** recupera a porcentagem de download concluído.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **downloadProgress**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Quando o controle do Windows Media Player está conectado a um arquivo de mídia que pode ser reproduzido e baixado ao mesmo tempo, a propriedade **downloadProgress** retorna a porcentagem do arquivo total que foi baixado. Atualmente, esse recurso tem suporte apenas em servidores Web. Os seguintes formatos de arquivo podem ser baixados e reproduzidos simultaneamente:

-   Advanced Systems Format (ASF)
-   Áudio do Windows Media (WMA)
-   Vídeo do Windows Media (WMV)
-   MP3
-   FUNCIONALIDADES
-   WAV
-   Alguns arquivos AVI

Use o *Player*. Evento de **buffer** para determinar quando o download começa e termina.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **downloadProgress** para exibir a porcentagem de download concluído. As informações são exibidas em um DIV HTML criado com ID = "DP". O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição. O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Evento Player. buffering**](player-player-buffering.md)
</dt> </dl>

 

 





