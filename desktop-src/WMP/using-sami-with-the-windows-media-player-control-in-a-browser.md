---
title: Usando SAMI com o controle do Windows Media Player em um navegador
description: Usando SAMI com o controle do Windows Media Player em um navegador
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- Arquivos SAMI (intercâmbio de mídia acessível) sincronizados
- SAMI (sincronizado com o intercâmbio de mídia acessível), arquivos
- SAMI (intercâmbio de mídia acessível), código de exemplo
- SAMI (sincronizado com o intercâmbio de mídia acessível), código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b651c3af117942d56ffc5334323913d26cdf6f99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916609"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a><span data-ttu-id="a3670-114">Usando SAMI com o controle do Windows Media Player em um navegador</span><span class="sxs-lookup"><span data-stu-id="a3670-114">Using SAMI with the Windows Media Player Control in a Browser</span></span>

<span data-ttu-id="a3670-115">Em vez de criar um arquivo SAMI para cada estilo de fonte ou linguagem, você pode declarar classes de estilo diferentes em um arquivo usando scripts básicos e o modelo de objeto de controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a3670-115">Instead of creating a SAMI file for each font style or language, you can declare different style classes in one file by using basic scripting and the Windows Media Player control object model.</span></span> <span data-ttu-id="a3670-116">Você pode criar controles personalizados que permitem que o usuário escolha entre as diferentes opções de estilo e idioma.</span><span class="sxs-lookup"><span data-stu-id="a3670-116">You can create custom controls that enable the user to choose between the different style and language options.</span></span> <span data-ttu-id="a3670-117">Além disso, você tem controle total sobre o design da interface do Player e a personalização de cada função.</span><span class="sxs-lookup"><span data-stu-id="a3670-117">Furthermore, you have complete control over the design of the Player interface and the customization of each function.</span></span>

<span data-ttu-id="a3670-118">Para obter informações detalhadas sobre como inserir o controle do Windows Media Player em uma página [da Web, consulte um exemplo simples de script em uma página da Web](simple-example-of-scripting-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="a3670-118">For detailed information about embedding the Windows Media Player control in a webpage, see [Simple Example of Scripting in a Web Page](simple-example-of-scripting-in-a-web-page.md).</span></span>

<span data-ttu-id="a3670-119">O código de exemplo a seguir demonstra como usar legendas codificadas com o controle do Windows Media Player incorporado em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="a3670-119">The following example code demonstrates how to use closed captions with the Windows Media Player control embedded in a webpage.</span></span> <span data-ttu-id="a3670-120">Ele inclui controles para permitir que o usuário selecione estilo de fonte e idioma.</span><span class="sxs-lookup"><span data-stu-id="a3670-120">It includes controls to allow the user to select font style and language.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a3670-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3670-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3670-122">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="a3670-122">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




