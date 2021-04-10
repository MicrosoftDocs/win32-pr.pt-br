---
title: Depurando código
description: Depurando código
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Capas do Windows Media Player, código de depuração
- capas, código de depuração
- código de depuração para capas
- Capas do Windows Media Player, registro em log
- capas, registro em log
- funcionalidade de registro em log em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292697"
---
# <a name="debugging-code"></a><span data-ttu-id="7d7bd-109">Depurando código</span><span class="sxs-lookup"><span data-stu-id="7d7bd-109">Debugging Code</span></span>

<span data-ttu-id="7d7bd-110">Geralmente, você desejará ver o que está acontecendo na sua capa.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-110">You often will want to see what is happening inside your skin.</span></span> <span data-ttu-id="7d7bd-111">Você pode fazer isso por meio de um controle de texto ou de um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-111">You can do this through a text control or through a log file.</span></span>

<span data-ttu-id="7d7bd-112">Você pode criar um elemento de **texto** e colocá-lo em uma parte da sua capa temporariamente.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-112">You can create a **TEXT** element and place it on a part of your skin temporarily.</span></span> <span data-ttu-id="7d7bd-113">Por exemplo, você pode usar o seguinte código para criar seu elemento de **texto** :</span><span class="sxs-lookup"><span data-stu-id="7d7bd-113">For example, you could use the following code to create your **TEXT** element:</span></span>


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



<span data-ttu-id="7d7bd-114">Em seguida, por exemplo, se você quiser ver a posição atual do conteúdo de mídia digital no Windows Media Player, poderá usar um código semelhante ao seguinte para exibir a posição atual na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-114">Then, for example, if you want to see the current position of the digital media content in Windows Media Player, you could use code similar to the following to display the current position in the text box.</span></span>


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a><span data-ttu-id="7d7bd-115">Para gravar informações de depuração em um arquivo de log</span><span class="sxs-lookup"><span data-stu-id="7d7bd-115">To Write Debugging Information to a Log File</span></span>

<span data-ttu-id="7d7bd-116">Para habilitar ou desabilitar a depuração, altere o valor da seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="7d7bd-116">To enable or disable debugging, change the value of the following registry key:</span></span>

<span data-ttu-id="7d7bd-117">**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**</span><span class="sxs-lookup"><span data-stu-id="7d7bd-117">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\MediaPlayer\\Preferences\\ScriptDebugging**</span></span>

<span data-ttu-id="7d7bd-118">Quando você define o valor como 1, o registro em log é habilitado.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-118">When you set the value to 1, logging is enabled.</span></span> <span data-ttu-id="7d7bd-119">Quando você define o valor como 0 (o padrão), o registro em log é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-119">When you set the value to 0 (the default), logging is disabled.</span></span>

<span data-ttu-id="7d7bd-120">Se o registro em log estiver habilitado, um arquivo será colocado no computador do usuário na mesma pasta que a capa.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-120">If logging is enabled, a file will be placed on the user's computer in the same folder as the skin.</span></span> <span data-ttu-id="7d7bd-121">O arquivo será nomeado "*filename* \_ 0 \_log.txt", em que *filename* é o nome do arquivo de capa.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-121">The file will be named "*filename*\_0\_log.txt", where *filename* is the name of the skin file.</span></span> <span data-ttu-id="7d7bd-122">O código em sua capa pode gravar texto nesse arquivo usando o *tema*. método **logString** .</span><span class="sxs-lookup"><span data-stu-id="7d7bd-122">The code in your skin can write text to this file by using the *Theme*.**logString** method.</span></span> <span data-ttu-id="7d7bd-123">Isso pode ser útil se você quiser determinar o que está acontecendo dentro do seu código enquanto ele está em execução.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-123">This can be useful if you want to determine what is going on inside your code while it is running.</span></span> <span data-ttu-id="7d7bd-124">Observe que o arquivo de texto é codificado com caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-124">Note that the text file is encoded with Unicode characters.</span></span>

<span data-ttu-id="7d7bd-125">Quando o registro em log estiver habilitado e você tiver instalado um sistema de desenvolvimento que fornece recursos de depuração (como Microsoft Visual Studio), as exceções que não são tratadas pelo código de script farão com que uma caixa de diálogo de aviso do depurador seja aberta para cada exceção.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-125">When logging is enabled and you have installed a development system that provides debugging capabilities (such as Microsoft Visual Studio), exceptions that are not handled by your script code will cause a debugger warning dialog box to open for each exception.</span></span> <span data-ttu-id="7d7bd-126">Esse é um recurso útil para ajudá-lo a depurar seu código de script.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-126">This is a useful feature to help you debug your script code.</span></span> <span data-ttu-id="7d7bd-127">Além disso, você pode anexar manualmente o processo do Windows Media Player ao seu depurador quando o log estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-127">Also, you can manually attach the Windows Media Player process to your debugger when logging is enabled.</span></span>

<span data-ttu-id="7d7bd-128">Esse SDK inclui uma capa de exemplo, chamada "logging", que demonstra a funcionalidade de log em capas.</span><span class="sxs-lookup"><span data-stu-id="7d7bd-128">This SDK includes a sample skin, called "logging", that demonstrates logging functionality in skins.</span></span> <span data-ttu-id="7d7bd-129">Para saber mais sobre como usar os exemplos, consulte [exemplos](samples.md).</span><span class="sxs-lookup"><span data-stu-id="7d7bd-129">To learn more about using the samples, see [Samples](samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d7bd-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d7bd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d7bd-131">**Sobre as capas**</span><span class="sxs-lookup"><span data-stu-id="7d7bd-131">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




