---
title: Usando SAMI com o Windows Media Player controle em um navegador
description: Usando SAMI com o Windows Media Player controle em um navegador
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Windows Media Player,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player de objeto, SAMI (Synchronized Accessible Media Interchange)
- modelo de objeto, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player ActiveX controle,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Controle ActiveX dispositivo móvel, SAMI (Synchronized Accessible Media Interchange)
- ActiveX controle,SAMI (Synchronized Accessible Media Interchange)
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), arquivos
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), arquivos
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), código de exemplo
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d277f2849e6036d85bc8c03940a7dbd59df8b81083ca88240ebd68be768fde9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134339"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a>Usando SAMI com o Windows Media Player controle em um navegador

Em vez de criar um arquivo SAMI para cada linguagem ou estilo de fonte, você pode declarar classes de estilo diferentes em um arquivo usando scripts básicos e o modelo de objeto Windows Media Player controle. Você pode criar controles personalizados que permitem que o usuário escolha entre as diferentes opções de estilo e idioma. Além disso, você tem controle total sobre o design da interface player e a personalização de cada função.

Para obter informações detalhadas sobre como Windows Media Player controle de Windows Media Player em uma página da Web, consulte Exemplo simples de [script em uma página da Web](simple-example-of-scripting-in-a-web-page.md).

O código de exemplo a seguir demonstra como usar legendas fechadas com o controle Windows Media Player inserido em uma página da Web. Ele inclui controles para permitir que o usuário selecione o estilo e o idioma da fonte.


```C++
<HTML>
<HEAD>

<SCRIPT>
  // The following variable is used to prevent multiple initialization.
  var initialized = false;
  // The following function populates the select boxes.
  // It is called the first time the media file is opened.
  // Before then, the SAMI settings cannot be retrieved.
  function initialize() {
    var newOption;
    for (var i = 0; i < Player.closedCaption.SAMILangCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMILangName(i);
      newOption.value = newOption.text;
      CCLang.options.add(newOption);
    }
    for (var i = 0; i < Player.closedCaption.SAMIStyleCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMIStyleName(i);
      newOption.value = newOption.text;
      CCStyle.options.add(newOption);
    }
    initialized = true;
  }
</SCRIPT>

<!-- The following script code runs when the page is fully loaded. -->
<SCRIPT for="window" event="onload()">
  Player.closedCaption.captioningID = "captions";
  Player.closedCaption.SAMIFileName = "https://www.proseware.com/Media/seattle.smi";
  // The digital media file will open automatically, after which
  // the OpenStateChange event (handled below) will fire.
  Player.URL = "https://www.proseware.com/Media/seattle.wmv";
</SCRIPT>

<!-- The following script code runs when a media file is opened. -->
<SCRIPT for="Player" event="OpenStateChange(NewState)">
  // The first time this event fires, the Player stops and the 
  // initialize function is called. This allows the user to 
  // select a language and style before viewing the file.
  if (13 == NewState && !initialized) {
    Player.controls.stop();
    initialize();
  }
</SCRIPT>

</HEAD>
<BODY>

<OBJECT 
  ID="Player" 
  classID="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"
  height="200" 
  width="250"
>
</OBJECT>

<TABLE height="100" width="250" border="3" bordercolor="blue">
  <TR align="center">
    <TD bgcolor="white">
      <SELECT ID="CCLang" onClick="Player.closedCaption.SAMILang = value"></SELECT>
      <SELECT ID="CCStyle" onClick="Player.closedCaption.SAMIStyle = value"></SELECT>
    </TD>
  </TR>
  <TR height="75">
    <TD bgcolor="blue">
      <DIV id="captions"></DIV>
    </TD>
  </TR>
</TABLE>

</BODY>
</HTML>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




