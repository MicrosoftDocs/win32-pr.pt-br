---
title: Garantindo que o Windows Media Player Abra o conteúdo do HTMLView
description: Garantindo que o Windows Media Player Abra o conteúdo do HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Listas de reprodução do metarquivo do Windows Media, Windows Media Player abrindo conteúdo do HTMLView
- listas de reprodução, Windows Media Player abrindo conteúdo do HTMLView
- listas de reprodução de metarquivo, Windows Media Player abrindo conteúdo HTMLView
- Playlists do metarquivo do Windows Media, abrindo conteúdo do HTMLView
- listas de reprodução, abrindo conteúdo do HTMLView
- listas de reprodução de metarquivo, abrindo conteúdo de HTMLView
- abrindo conteúdo do HTMLView
- Windows Media Player, abrindo conteúdo do HTMLView
- Windows Media Player, conteúdo do HTMLView
- HTMLView, abrindo conteúdo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636060"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a><span data-ttu-id="da68a-113">Garantindo que o Windows Media Player Abra o conteúdo do HTMLView</span><span class="sxs-lookup"><span data-stu-id="da68a-113">Ensuring that Windows Media Player Opens the HTMLView Content</span></span>

<span data-ttu-id="da68a-114">Atualmente, o Windows Media Player 9 Series e o Windows Media Player 10 são os únicos players que oferecem suporte ao parâmetro *HtmlView* em arquivos. asx.</span><span class="sxs-lookup"><span data-stu-id="da68a-114">Currently, Windows Media Player 9 Series and Windows Media Player 10 are the only players that support the *HTMLView* parameter in .asx files.</span></span> <span data-ttu-id="da68a-115">Isso significa que você deve tomar medidas para garantir que o conteúdo do HTMLView seja reproduzido nessas versões do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="da68a-115">This means you should take steps to ensure that your HTMLView content plays back in these versions of Windows Media Player.</span></span>

<span data-ttu-id="da68a-116">Primeiro, você deve determinar se o Windows Media Player 9 Series ou o Windows Media Player 10 está instalado no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="da68a-116">You must first determine whether Windows Media Player 9 Series or Windows Media Player 10 is installed on the user's computer.</span></span> <span data-ttu-id="da68a-117">O SDK do Windows Media Player inclui um exemplo abrangente que demonstra como detectar diferentes versões do Windows Media Player em diferentes navegadores da Web.</span><span class="sxs-lookup"><span data-stu-id="da68a-117">The Windows Media Player SDK includes a comprehensive sample that demonstrates how to detect different versions of Windows Media Player in different Web browsers.</span></span> <span data-ttu-id="da68a-118">Embora uma análise completa da amostra de detecção esteja além do escopo desta seção, há algumas etapas básicas que podem ser seguidas para determinar qual versão do Windows Media Player o computador do usuário está executando.</span><span class="sxs-lookup"><span data-stu-id="da68a-118">Although a complete analysis of the detection sample is beyond the scope of this section, there are some basic steps you can take to determine which version of Windows Media Player the user's computer is running.</span></span>

<span data-ttu-id="da68a-119">Em sua forma mais simples, detectar o Windows Media Player envolve inserir o controle do jogador na página da Web que vincula ao conteúdo do HTMLView e, em seguida, inspecionando o valor recuperado pelo *Player*. Propriedade **versionInfo** .</span><span class="sxs-lookup"><span data-stu-id="da68a-119">In its simplest form, detecting Windows Media Player involves embedding the Player control in the webpage that links to your HTMLView content and then inspecting the value retrieved by the *Player*.**versionInfo** property.</span></span> <span data-ttu-id="da68a-120">Depois de verificar se o usuário tem o Windows Media Player 9 Series ou o Windows Media Player 10 instalado, você pode usar o método [Player. openPlayer](player-openplayer.md) para abrir o conteúdo no player de modo completo.</span><span class="sxs-lookup"><span data-stu-id="da68a-120">Once you have verified that the user has Windows Media Player 9 Series or Windows Media Player 10 installed, you can use the [Player.openPlayer](player-openplayer.md) method to open the content in the full-mode Player.</span></span> <span data-ttu-id="da68a-121">O método **openPlayer** garante que seu conteúdo seja inicialmente exibido no recurso em **execução** do player de modo completo, em vez de em uma capa, no modo de mini Player ou em outro player que se registrou como programa padrão para arquivos com uma extensão de nome de arquivo. ASX, mas não dá suporte a HtmlView.</span><span class="sxs-lookup"><span data-stu-id="da68a-121">The **openPlayer** method ensures that your content is initially displayed in the **Now Playing** feature of the full-mode Player, rather than in a skin, in mini Player mode, or in another player that has registered itself as the default program for files with an .asx file name extension, but doesn't support HTMLView.</span></span> <span data-ttu-id="da68a-122">No entanto, quando o conteúdo é exibido, o usuário tem o controle total do Windows Media Player, o que significa que ele pode optar por exibir um recurso diferente de **agora em execução**, alternar para o modo de capa ou até mesmo sair do Player.</span><span class="sxs-lookup"><span data-stu-id="da68a-122">Once the content is displayed, however, the user has complete control of Windows Media Player, meaning that he or she can choose to display a feature other than **Now Playing**, switch to skin mode, or even quit the Player.</span></span>

<span data-ttu-id="da68a-123">O código de exemplo a seguir cria uma página da Web para o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="da68a-123">The following example code creates a webpage for Internet Explorer.</span></span> <span data-ttu-id="da68a-124">Essa página abre um arquivo. ASX, que especifica uma página da Web HTMLView que aparece no player de modo completo quando o Windows Media Player 9 Series ou posterior está instalado.</span><span class="sxs-lookup"><span data-stu-id="da68a-124">This page opens an .asx file, which specifies an HTMLView webpage that appears in the full-mode Player when Windows Media Player 9 Series or later is installed.</span></span>


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="da68a-125">O código no exemplo anterior incorpora o controle do Windows Media Player com a propriedade **UIMODE** definida como "invisível" e os atributos de altura e largura do Player são definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="da68a-125">The code in the preceding example embeds the Windows Media Player control with the **uiMode** property set to "invisible" and the Player height and width attributes set to zero.</span></span> <span data-ttu-id="da68a-126">Isso ocorre porque a página da Web não exige que a interface do usuário de controle do jogador seja exibida inicialmente — ela só requer acesso ao modelo de objeto do Player.</span><span class="sxs-lookup"><span data-stu-id="da68a-126">This is because the webpage does not require the Player control user interface to be displayed initially—it only requires access to the Player object model.</span></span> <span data-ttu-id="da68a-127">A página também exibe um botão de entrada que permite ao usuário reproduzir o arquivo. asx.</span><span class="sxs-lookup"><span data-stu-id="da68a-127">The page also displays an input button that enables the user to play the .asx file.</span></span>

<span data-ttu-id="da68a-128">Quando o usuário clica no botão reproduzir ASX, a função PlayASX do Microsoft JScript é executada.</span><span class="sxs-lookup"><span data-stu-id="da68a-128">When the user clicks the Play ASX button, the Microsoft JScript function PlayASX runs.</span></span> <span data-ttu-id="da68a-129">Essa função primeiro recupera o valor para a propriedade **versionInfo** do Player, usando o método **parseInt** do JScript para inspecionar o valor numérico da cadeia de caracteres recuperada.</span><span class="sxs-lookup"><span data-stu-id="da68a-129">This function first retrieves the value for the Player **versionInfo** property, using the JScript **parseInt** method to inspect the numerical value of the string retrieved.</span></span> <span data-ttu-id="da68a-130">Se o valor numérico for maior ou igual a 9 (o que significa que o usuário tem o Windows Media Player 9 Series instalado), o código do script chamará o método **openPlayer** , passando a URL do arquivo. asx que contém o parâmetro HtmlView.</span><span class="sxs-lookup"><span data-stu-id="da68a-130">If the numerical value is greater than or equal to 9 (meaning that the user has Windows Media Player 9 Series installed), the script code calls the **openPlayer** method, passing the URL of the .asx file that contains the HTMLView parameter.</span></span> <span data-ttu-id="da68a-131">Esse método abre o arquivo. asx usando o Windows Media Player no modo completo, desempenha o conteúdo de mídia digital na lista de reprodução. ASX e exibe o conteúdo baseado na Web do HTMLView no recurso de **agora em execução** .</span><span class="sxs-lookup"><span data-stu-id="da68a-131">This method opens the .asx file using Windows Media Player in full mode, plays the digital media content in the .asx playlist, and displays the HTMLView Web-based content in the **Now Playing** feature.</span></span>

<span data-ttu-id="da68a-132">Se o valor numérico da cadeia de caracteres da versão não for maior ou igual a 9 (o que significa que o usuário não tem o Windows Media Player 9 Series ou posterior instalado em seu computador), o código de script altera o **UIMODE** do controle Player para "Full", define uma nova largura e altura para o controle e, em seguida, abre o arquivo. ASX no player incorporado especificando um valor para a propriedade **URL** .</span><span class="sxs-lookup"><span data-stu-id="da68a-132">If the numerical value of the version string is not greater than or equal to 9 (meaning that the user does not have Windows Media Player 9 Series or later installed on his or her computer), the script code changes the **uiMode** of the Player control to "full", sets a new width and height for the control, and then opens the .asx file in the embedded Player by specifying a value for the **URL** property.</span></span> <span data-ttu-id="da68a-133">Quando isso acontece, o conteúdo de mídia digital é executado na página da Web, mas todos os valores de HTMLView especificados no arquivo. asx são ignorados.</span><span class="sxs-lookup"><span data-stu-id="da68a-133">When this happens, the digital media content plays in the webpage, but any HTMLView values specified in the .asx file are ignored.</span></span>

<span data-ttu-id="da68a-134">Como o conteúdo é reproduzido quando o usuário não tem o Windows Media Player 9 Series ou o Windows Media Player 10 instalado cabe a você.</span><span class="sxs-lookup"><span data-stu-id="da68a-134">How content is played back when the user does not have Windows Media Player 9 Series or Windows Media Player 10 installed is up to you.</span></span> <span data-ttu-id="da68a-135">O exemplo anterior mostra como especificar que o conteúdo é tocado na página da Web em vez do player de modo completo, ignorando qualquer conteúdo de HTMLView no processo.</span><span class="sxs-lookup"><span data-stu-id="da68a-135">The preceding example shows how to specify that the content play in the webpage instead of the full-mode Player, ignoring any HTMLView content in the process.</span></span> <span data-ttu-id="da68a-136">Há outras abordagens que você pode tomar.</span><span class="sxs-lookup"><span data-stu-id="da68a-136">There are other approaches you might take.</span></span> <span data-ttu-id="da68a-137">Por exemplo, você pode solicitar que o usuário instale uma versão mais recente do Windows Media Player, tornando essa versão do Player um requisito para reproduzir seu conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="da68a-137">For example, you could prompt the user to install a newer version of Windows Media Player, making that version of the Player a requirement for playing back your digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da68a-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da68a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da68a-139">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="da68a-139">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="da68a-140">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="da68a-140">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="da68a-141">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="da68a-141">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 




