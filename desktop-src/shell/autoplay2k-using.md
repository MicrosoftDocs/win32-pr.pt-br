---
description: Quando o Shell detecta a inserção de uma nova mídia ou o anexo de um dispositivo de hot-plug, o conteúdo do dispositivo ou da mídia é determinado. A reprodução automática, dependendo de suas configurações atuais, realiza uma das ações a seguir.
title: Usando e configurando a reprodução automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646850"
---
# <a name="using-and-configuring-autoplay"></a><span data-ttu-id="d9ea3-104">Usando e configurando a reprodução automática</span><span class="sxs-lookup"><span data-stu-id="d9ea3-104">Using and Configuring AutoPlay</span></span>

<span data-ttu-id="d9ea3-105">Quando o Shell detecta a inserção de uma nova mídia ou o anexo de um dispositivo de hot-plug, o conteúdo do dispositivo ou da mídia é determinado.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-105">When the Shell detects the insertion of new media or the attachment of a hot-plug device, the contents of the device or media are determined.</span></span> <span data-ttu-id="d9ea3-106">A reprodução automática, dependendo de suas configurações atuais, realiza uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-106">AutoPlay, depending on its current settings, does one of the following.</span></span>

-   <span data-ttu-id="d9ea3-107">Reproduz o conteúdo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-107">Plays the content automatically.</span></span>
-   <span data-ttu-id="d9ea3-108">Exibe uma caixa de diálogo solicitando que o usuário escolha um manipulador padrão para um único tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-108">Displays a dialog box prompting the user to choose a default handler for a single content type.</span></span>
-   <span data-ttu-id="d9ea3-109">Apresenta, no caso de conteúdo misto, uma lista de aplicativos de manipuladores disponíveis a serem iniciados.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-109">Presents, in the case of mixed content, a list of available handler applications to launch.</span></span> <span data-ttu-id="d9ea3-110">O manipulador escolhido, em seguida, executa automaticamente seu tipo de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-110">The chosen handler then automatically plays its associated content type.</span></span>
-   <span data-ttu-id="d9ea3-111">Exibe uma exibição de pasta padrão dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-111">Displays a standard folder view of the files.</span></span>
-   <span data-ttu-id="d9ea3-112">Não faz nada se, anteriormente, o usuário tivesse escolhido não **executar nenhuma ação** para esse tipo de conteúdo, bem como o especificado **sempre faz a ação selecionada**.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-112">Does nothing if, earlier, the user had chosen **Take no action** for that content type as well as specified **Always do the selected action**.</span></span>

<span data-ttu-id="d9ea3-113">Se o conteúdo não atender aos critérios de reprodução automática, o evento será passado para a WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-113">If the contents do not meet the criteria for AutoPlay, the event is then passed to Windows Image Acquisition (WIA).</span></span>

<span data-ttu-id="d9ea3-114">Os tópicos a seguir abordam a configuração e o uso da reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-114">The following topics discuss the setup and use of AutoPlay.</span></span>

-   [<span data-ttu-id="d9ea3-115">Preparando o hardware e o software para uso com a reprodução automática</span><span class="sxs-lookup"><span data-stu-id="d9ea3-115">Preparing Hardware and Software for Use with AutoPlay</span></span>](#preparing-hardware-and-software-for-use-with-autoplay)
-   [<span data-ttu-id="d9ea3-116">Como a reprodução automática pesquisa mídia</span><span class="sxs-lookup"><span data-stu-id="d9ea3-116">How AutoPlay Searches Media</span></span>](#how-autoplay-searches-media)
-   [<span data-ttu-id="d9ea3-117">Definindo tipos de conteúdo únicos e mistos</span><span class="sxs-lookup"><span data-stu-id="d9ea3-117">Defining Single and Mixed Content Types</span></span>](#defining-single-and-mixed-content-types)
-   [<span data-ttu-id="d9ea3-118">Cenários de exemplo</span><span class="sxs-lookup"><span data-stu-id="d9ea3-118">Sample Scenarios</span></span>](#sample-scenarios)
    -   [<span data-ttu-id="d9ea3-119">Reprodução automática para dispositivos de armazenamento com mídia de imagem</span><span class="sxs-lookup"><span data-stu-id="d9ea3-119">AutoPlay for Storage Devices with Picture Media</span></span>](#autoplay-for-storage-devices-with-picture-media)
    -   [<span data-ttu-id="d9ea3-120">Reprodução automática de dispositivos de música e dispositivos de armazenamento com mídia de música</span><span class="sxs-lookup"><span data-stu-id="d9ea3-120">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [<span data-ttu-id="d9ea3-121">Reprodução automática para reprodução de vídeo na primeira apresentação</span><span class="sxs-lookup"><span data-stu-id="d9ea3-121">AutoPlay for Video Playback on First Presentation</span></span>](#autoplay-for-video-playback-on-first-presentation)
-   [<span data-ttu-id="d9ea3-122">Atribuindo aplicativos de manipulador padrão</span><span class="sxs-lookup"><span data-stu-id="d9ea3-122">Assigning Default Handler Applications</span></span>](#assigning-default-handler-applications)
-   [<span data-ttu-id="d9ea3-123">Manipulando mídia que contém tipos de conteúdo mistos</span><span class="sxs-lookup"><span data-stu-id="d9ea3-123">Handling Media Containing Mixed Content Types</span></span>](#handling-media-containing-mixed-content-types)
-   [<span data-ttu-id="d9ea3-124">Interfaces do usuário de reprodução automática</span><span class="sxs-lookup"><span data-stu-id="d9ea3-124">AutoPlay User Interfaces</span></span>](#autoplay-user-interfaces)
    -   [<span data-ttu-id="d9ea3-125">Caixa de diálogo tipo de conteúdo único</span><span class="sxs-lookup"><span data-stu-id="d9ea3-125">Single Content Type Dialog Box</span></span>](#single-content-type-dialog-box)
    -   [<span data-ttu-id="d9ea3-126">Caixa de diálogo mídia mista</span><span class="sxs-lookup"><span data-stu-id="d9ea3-126">Mixed Media Dialog Box</span></span>](#mixed-media-dialog-box)
    -   [<span data-ttu-id="d9ea3-127">Página de Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9ea3-127">Property Page</span></span>](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a><span data-ttu-id="d9ea3-128">Preparando o hardware e o software para uso com a reprodução automática</span><span class="sxs-lookup"><span data-stu-id="d9ea3-128">Preparing Hardware and Software for Use with AutoPlay</span></span>

<span data-ttu-id="d9ea3-129">Várias informações precisam aparecer no registro para que a reprodução automática funcione.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-129">Several pieces of information need to appear in the registry for AutoPlay to function.</span></span> <span data-ttu-id="d9ea3-130">Essas informações interagem e fazem referência umas às outras para formar o ambiente completo de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-130">These pieces of information interact and reference each other to form the full AutoPlay environment.</span></span> <span data-ttu-id="d9ea3-131">Este documento apresenta a configuração de cada uma dessas informações como um procedimento autônomo individual.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-131">This document presents the setup of each of these pieces of information as an individual stand-alone procedure.</span></span>

<span data-ttu-id="d9ea3-132">Consulte os tópicos a seguir para obter instruções adicionais.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-132">See the following topics for additional instructions.</span></span>

-   [<span data-ttu-id="d9ea3-133">Como atribuir um manipulador de dispositivo a um dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9ea3-133">How To Assign a Device Handler to a Device</span></span>](how-to-assign-a-device-handler-to-a-device.md)
-   [<span data-ttu-id="d9ea3-134">Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando um grupo de dispositivos</span><span class="sxs-lookup"><span data-stu-id="d9ea3-134">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [<span data-ttu-id="d9ea3-135">Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando uma classe de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9ea3-135">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [<span data-ttu-id="d9ea3-136">Como evitar a reprodução automática para um componente</span><span class="sxs-lookup"><span data-stu-id="d9ea3-136">How To Prevent AutoPlay for a Component</span></span>](how-to-prevent-autoplay-for-a-component.md)
-   [<span data-ttu-id="d9ea3-137">Como registrar um manipulador para um evento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9ea3-137">How To Register a Handler for a Device Event</span></span>](how-to-register-a-handler-for-a-device-event.md)
-   [<span data-ttu-id="d9ea3-138">Como usar eventos de reprodução automática em aplicativos em execução</span><span class="sxs-lookup"><span data-stu-id="d9ea3-138">How To Use AutoPlay Events in Running Applications</span></span>](how-to-use-autoplay-events-in-running-applications.md)
-   [<span data-ttu-id="d9ea3-139">Como registrar um manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="d9ea3-139">How To Register an Event Handler</span></span>](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a><span data-ttu-id="d9ea3-140">Como a reprodução automática pesquisa mídia</span><span class="sxs-lookup"><span data-stu-id="d9ea3-140">How AutoPlay Searches Media</span></span>

<span data-ttu-id="d9ea3-141">A reprodução automática pesquisa quatro níveis de diretório de mídia abaixo do diretório raiz para encontrar tipos de arquivos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-141">AutoPlay searches for media four directory levels below the root directory to find known file types.</span></span> <span data-ttu-id="d9ea3-142">Ele usa o valor percebido associado a uma extensão de nome de arquivo no registro para determinar a categoria do arquivo, seja uma imagem, um arquivo de áudio ou um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-142">It uses the PerceivedType value associated with a file name extension in the registry to determine the file category, whether it is an image, an audio file, or a video file.</span></span> <span data-ttu-id="d9ea3-143">Com essas informações, a reprodução automática inicia o manipulador apropriado para esse dispositivo e tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-143">With this information, AutoPlay launches the appropriate handler for that device and file type.</span></span> <span data-ttu-id="d9ea3-144">Para obter mais informações, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-144">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="defining-single-and-mixed-content-types"></a><span data-ttu-id="d9ea3-145">Definindo tipos de conteúdo únicos e mistos</span><span class="sxs-lookup"><span data-stu-id="d9ea3-145">Defining Single and Mixed Content Types</span></span>

<span data-ttu-id="d9ea3-146">A reprodução automática define três categorias de conteúdo principal.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-146">AutoPlay defines three main content categories.</span></span>

-   <span data-ttu-id="d9ea3-147">Imagens</span><span class="sxs-lookup"><span data-stu-id="d9ea3-147">Pictures</span></span>
-   <span data-ttu-id="d9ea3-148">Música</span><span class="sxs-lookup"><span data-stu-id="d9ea3-148">Music</span></span>
-   <span data-ttu-id="d9ea3-149">Vídeo</span><span class="sxs-lookup"><span data-stu-id="d9ea3-149">Video</span></span>

<span data-ttu-id="d9ea3-150">Uma mídia é considerada para conter um único tipo de conteúdo se todos os arquivos na mídia se enquadram em apenas uma dessas três categorias.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-150">A medium is considered to contain a single content type if all of the files on the medium fall into only one of these three categories.</span></span> <span data-ttu-id="d9ea3-151">Observe que isso não significa que os arquivos devem ser do mesmo tipo de *arquivo* ;. jpg,. gif e. bmp são tipos de arquivo diferentes, mas um tipo de conteúdo (imagens).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-151">Note that this does not mean that the files must be of the same *file* type; .jpg, .gif, and .bmp are different file types, but one content type (pictures).</span></span>

<span data-ttu-id="d9ea3-152">Se os tipos de conteúdo com suporte estiverem presentes na mídia, mas nenhum tipo de conteúdo único puder considerar 100 por cento do total, a mídia será considerada para conter o tipo de conteúdo misto e será manipulada de acordo.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-152">If supported content types are present on the medium, but no single content type can account for 100 percent of the total, then the medium is considered to contain mixed content type and is handled accordingly.</span></span> <span data-ttu-id="d9ea3-153">Para obter mais informações, consulte [manipulando mídia que contém tipos de conteúdo mistos](#handling-media-containing-mixed-content-types).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-153">For more information, see [Handling Media Containing Mixed Content Types](#handling-media-containing-mixed-content-types).</span></span>

## <a name="sample-scenarios"></a><span data-ttu-id="d9ea3-154">Cenários de Exemplo</span><span class="sxs-lookup"><span data-stu-id="d9ea3-154">Sample Scenarios</span></span>

<span data-ttu-id="d9ea3-155">Os cenários a seguir fornecem uma compreensão básica do que esperar da reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-155">The following scenarios provide a basic understanding of what to expect from AutoPlay.</span></span>

### <a name="autoplay-for-storage-devices-with-picture-media"></a><span data-ttu-id="d9ea3-156">Reprodução automática para dispositivos de armazenamento com mídia de imagem</span><span class="sxs-lookup"><span data-stu-id="d9ea3-156">AutoPlay for Storage Devices with Picture Media</span></span>

1.  <span data-ttu-id="d9ea3-157">O usuário anexa um dispositivo de leitor USB SanDisk CompactFlash que já tem mídia inserida contendo o tipo de conteúdo de imagem de 100% na forma de arquivos. jpg.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-157">The user attaches a USB SanDisk CompactFlash reader device that already has media inserted containing 100 percent picture content type in the form of .jpg files.</span></span>
2.  <span data-ttu-id="d9ea3-158">As exibições **de notificação encontraram novo hardware – SanDisk ImageMate**.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-158">Notification displays **Found New Hardware - SanDisk ImageMate**.</span></span>
3.  <span data-ttu-id="d9ea3-159">A reprodução automática inicia o aplicativo de imagem apropriado.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-159">AutoPlay launches the appropriate image application.</span></span>

<span data-ttu-id="d9ea3-160">Da mesma forma, quando o usuário insere essa mesma mídia do CompactFlash no leitor quando o leitor já está anexado ao sistema, o evento de inserção de mídia também faz com que a reprodução automática inicie o aplicativo de apresentação de slides de imagem.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-160">Similarly, when the user inserts that same CompactFlash media into the reader when the reader is already attached to the system, the media insert event also causes AutoPlay to launch the image slide show application.</span></span> <span data-ttu-id="d9ea3-161">O usuário tem a opção de ir para a página de propriedades do dispositivo de mídia SanDisk para alterar o padrão para outro aplicativo de reprodução automática registrado, como o assistente de scanner e câmera ou o Picture It!.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-161">The user has the option of going to the Properties page of the SanDisk media device to change the default to another registered AutoPlay application, such as the Scanner and Camera Wizard or Picture It!.</span></span>

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a><span data-ttu-id="d9ea3-162">Reprodução automática de dispositivos de música e dispositivos de armazenamento com mídia de música</span><span class="sxs-lookup"><span data-stu-id="d9ea3-162">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>

1.  <span data-ttu-id="d9ea3-163">O usuário anexa um player de MP3 USB Diamond Rio.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-163">The user attaches a USB Diamond Rio MP3 Player.</span></span>
2.  <span data-ttu-id="d9ea3-164">As telas de notificação **encontraram um novo hardware-Diamond Rio MP3 Player**.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-164">Notification displays **Found New Hardware - Diamond Rio MP3 Player**.</span></span>
3.  <span data-ttu-id="d9ea3-165">A reprodução automática reproduz os arquivos usando seu manipulador padrão registrado — por exemplo, o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-165">AutoPlay plays the files using its registered default handler—for instance, Windows Media Player.</span></span>

<span data-ttu-id="d9ea3-166">Da mesma forma, se o usuário insere qualquer mídia contendo arquivos. mp3 (por exemplo, CompactFlash, SmartMedia, Memory Stick ou CD-ROM) que conta com 100% do conteúdo total com suporte em um dispositivo de armazenamento, o evento de inserção de mídia também faria com que a reprodução automática reproduza os arquivos usando o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-166">Similarly, if the user inserts any media containing .mp3 files (for example, CompactFlash, SmartMedia, Memory Stick, or CD-ROM) that account for 100 percent of the total supported content into a storage device, the media insert event would also cause AutoPlay to play the files using the Windows Media Player.</span></span> <span data-ttu-id="d9ea3-167">O usuário pode acessar a folha de propriedades do dispositivo de armazenamento e alterar a ação padrão para outro aplicativo de reprodução automática registrado, como WinAmp ou real player.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-167">The user can access the property sheet of the storage device and change the default action to another registered AutoPlay application, such as WinAmp or Real Player.</span></span>

### <a name="autoplay-for-video-playback-on-first-presentation"></a><span data-ttu-id="d9ea3-168">Reprodução automática para reprodução de vídeo na primeira apresentação</span><span class="sxs-lookup"><span data-stu-id="d9ea3-168">AutoPlay for Video Playback on First Presentation</span></span>

1.  <span data-ttu-id="d9ea3-169">O usuário conecta uma câmera de vídeo digital 1394 pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-169">The user plugs in a 1394 digital video camera for the first time.</span></span>
2.  <span data-ttu-id="d9ea3-170">O usuário recebe uma caixa de diálogo simples que pergunta qual aplicativo deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-170">The user is presented with a simple dialog box that asks what application to run.</span></span> <span data-ttu-id="d9ea3-171">As opções são executar um dos aplicativos de reprodução automática registrados ou abrir uma pasta para exibir arquivos.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-171">The choices are to run one of the registered AutoPlay applications or to open a folder to view files.</span></span> <span data-ttu-id="d9ea3-172">O usuário pode definir o comportamento selecionado para ser salvo como a ação padrão para eventos de hot-plug da câmera de vídeo digital posterior.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-172">The user may set the selected behavior to be saved as the default action for later digital video camera hot-plug events.</span></span>

## <a name="assigning-default-handler-applications"></a><span data-ttu-id="d9ea3-173">Atribuindo aplicativos de manipulador padrão</span><span class="sxs-lookup"><span data-stu-id="d9ea3-173">Assigning Default Handler Applications</span></span>

<span data-ttu-id="d9ea3-174">Uma nova instalação do Windows localiza a reprodução automática com um conjunto de aplicativos de manipulador registrados.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-174">A fresh installation of Windows finds AutoPlay with a set of registered handler applications.</span></span> <span data-ttu-id="d9ea3-175">Os aplicativos registrados por padrão durante uma instalação do Windows são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-175">Applications registered by default during a Windows installation are as follows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9ea3-176">Tipo de Mídia</span><span class="sxs-lookup"><span data-stu-id="d9ea3-176">Media Type</span></span></th>
<th><span data-ttu-id="d9ea3-177">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="d9ea3-177">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9ea3-178">Imagens</span><span class="sxs-lookup"><span data-stu-id="d9ea3-178">Pictures</span></span></td>
<td><ul>
<li><span data-ttu-id="d9ea3-179">Apresentação de slides (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9ea3-179">Slide Show (default)</span></span></li>
<li><span data-ttu-id="d9ea3-180">Assistente de câmera e scanner</span><span class="sxs-lookup"><span data-stu-id="d9ea3-180">Camera and Scanner Wizard</span></span></li>
<li><span data-ttu-id="d9ea3-181">Assistente de impressão</span><span class="sxs-lookup"><span data-stu-id="d9ea3-181">Printing Wizard</span></span></li>
<li><span data-ttu-id="d9ea3-182">Abrir pasta</span><span class="sxs-lookup"><span data-stu-id="d9ea3-182">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9ea3-183">Música</span><span class="sxs-lookup"><span data-stu-id="d9ea3-183">Music</span></span></td>
<td><ul>
<li><span data-ttu-id="d9ea3-184">Windows Media Player (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9ea3-184">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="d9ea3-185">Abrir pasta</span><span class="sxs-lookup"><span data-stu-id="d9ea3-185">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9ea3-186">Vídeo</span><span class="sxs-lookup"><span data-stu-id="d9ea3-186">Video</span></span></td>
<td><ul>
<li><span data-ttu-id="d9ea3-187">Windows Media Player (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9ea3-187">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="d9ea3-188">Abrir pasta</span><span class="sxs-lookup"><span data-stu-id="d9ea3-188">Open folder</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d9ea3-189">No caso de tipos sem suporte, os usuários são solicitados a atribuir a configuração padrão para a ação de reprodução automática associada a cada dispositivo de armazenamento na primeira introdução ao sistema.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-189">In the case of non-supported types, users are asked to assign the default setting for the AutoPlay action associated with each storage device on its first introduction to the system.</span></span> <span data-ttu-id="d9ea3-190">Nesse momento, o usuário será solicitado a escolher uma ação em uma lista fornecida de aplicativos registrados ou exibir uma exibição de pasta listando o conteúdo da mídia.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-190">At that time, the user is prompted to choose an action from a provided list of registered applications or to display a folder view listing the media content.</span></span> <span data-ttu-id="d9ea3-191">O usuário também tem a opção de escolher ser solicitada cada vez que o tipo de mídia for detectado, em vez de salvar qualquer aplicativo específico como padrão.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-191">The user also has the option of choosing to be prompted each time the media type is detected rather than saving any particular application as a default.</span></span>

> [!Note]  
> <span data-ttu-id="d9ea3-192">Os fabricantes de dispositivos têm a opção de registrar e atribuir aplicativos padrão a serem usados com seus produtos específicos.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-192">Device manufacturers have the option of registering and assigning default applications to be used with their particular products.</span></span> <span data-ttu-id="d9ea3-193">Nesses casos, a caixa de diálogo que oferece uma opção para o usuário não é exibida.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-193">In these cases, the dialog box offering a choice to the user is not displayed.</span></span>

 

<span data-ttu-id="d9ea3-194">Para ser oferecido como uma opção de manipulador por reprodução automática, os aplicativos recém-instalados devem se registrar no registro.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-194">To be offered as a handler option by AutoPlay, newly installed applications must register themselves in the registry.</span></span> <span data-ttu-id="d9ea3-195">Para obter detalhes, consulte [preparando o hardware e o software para uso com a reprodução automática](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-195">For details, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

<span data-ttu-id="d9ea3-196">Os usuários sempre podem alterar o manipulador de reprodução automática padrão para qualquer dispositivo de armazenamento ou tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-196">Users can always change the default AutoPlay handler for any storage device or content type.</span></span> <span data-ttu-id="d9ea3-197">A página de propriedades de reprodução automática pode ser acessada para alteração na folha de propriedades do dispositivo de armazenamento no **meu computador**.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-197">The AutoPlay property page is accessible for change in the property sheet of the storage device in **My Computer**.</span></span>

<span data-ttu-id="d9ea3-198">Para obter exemplos de prompts do usuário e páginas de propriedades, consulte [interfaces do usuário de reprodução automática](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-198">For examples of user prompts and property pages, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="handling-media-containing-mixed-content-types"></a><span data-ttu-id="d9ea3-199">Manipulando mídia que contém tipos de conteúdo mistos</span><span class="sxs-lookup"><span data-stu-id="d9ea3-199">Handling Media Containing Mixed Content Types</span></span>

<span data-ttu-id="d9ea3-200">Quando a reprodução automática é apresentada com um meio de conteúdo misto, ela requer entrada do usuário para que possa tomar medidas.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-200">When AutoPlay is presented with a mixed content medium, it requires user input before it can take action.</span></span> <span data-ttu-id="d9ea3-201">Nesse caso, o usuário recebe uma caixa de diálogo contendo uma lista filtrada de todos os aplicativos registrados apropriados disponíveis para os tipos de conteúdo presentes na mídia.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-201">In this case, the user is presented with a dialog box containing a filtered list of all appropriate registered applications available for the content types present on the media.</span></span> <span data-ttu-id="d9ea3-202">O usuário pode escolher um desses aplicativos para executar uma reprodução automática desse tipo de conteúdo específico, enquanto o restante permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-202">The user can choose one of these applications to AutoPlay that particular content type, while the rest remain untouched.</span></span> <span data-ttu-id="d9ea3-203">Como a composição de mídia de conteúdo misto varia de acordo com cada disco individual, não há nenhuma opção para salvar essa opção como padrão.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-203">As the composition of mixed content media varies with each individual disc, there is no option to save this choice as a default.</span></span>

<span data-ttu-id="d9ea3-204">Para obter exemplos de prompts do usuário, consulte [interfaces do usuário de reprodução automática](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-204">For examples of user prompts, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="autoplay-user-interfaces"></a><span data-ttu-id="d9ea3-205">Interfaces do usuário de reprodução automática</span><span class="sxs-lookup"><span data-stu-id="d9ea3-205">AutoPlay User Interfaces</span></span>

<span data-ttu-id="d9ea3-206">Há três interfaces de usuário possíveis.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-206">There are three possible user interfaces.</span></span>

-   <span data-ttu-id="d9ea3-207">Uma caixa de diálogo que solicita que o usuário insira uma ação para um único tipo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="d9ea3-207">A dialog box that prompts the user to enter an action for a single content type</span></span>
-   <span data-ttu-id="d9ea3-208">Uma caixa de diálogo que solicita que o usuário insira uma ação para tipos de conteúdo misto</span><span class="sxs-lookup"><span data-stu-id="d9ea3-208">A dialog box that prompts the user to enter an action for mixed content types</span></span>
-   <span data-ttu-id="d9ea3-209">Uma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="d9ea3-209">A property page</span></span>

### <a name="single-content-type-dialog-box"></a><span data-ttu-id="d9ea3-210">Caixa de diálogo tipo de conteúdo único</span><span class="sxs-lookup"><span data-stu-id="d9ea3-210">Single Content Type Dialog Box</span></span>

<span data-ttu-id="d9ea3-211">Uma caixa de diálogo semelhante à seguinte é exibida quando qualquer mídia com suporte ainda não atribuída a uma ação de reprodução automática é apresentada ao sistema.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-211">A dialog box similar to the following is displayed when any supported media not yet assigned a default AutoPlay action is presented to the system.</span></span>

![captura de tela da caixa de diálogo tipo de conteúdo único](images/pix.png)

<span data-ttu-id="d9ea3-213">Os usuários podem executar uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-213">Users can do one of the following.</span></span>

-   <span data-ttu-id="d9ea3-214">Escolha uma ação na lista de aplicativos registrados.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-214">Choose an action from the list of registered applications.</span></span>
-   <span data-ttu-id="d9ea3-215">Liste os arquivos na mídia em um modo de exibição de pasta normal.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-215">List the files on the medium in a normal folder view.</span></span>
-   <span data-ttu-id="d9ea3-216">Não executar nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-216">Take no action.</span></span>

<span data-ttu-id="d9ea3-217">Um usuário também pode salvar uma opção como a ação padrão para essa mídia clicando na caixa de **ação sempre fazer a seleção** .</span><span class="sxs-lookup"><span data-stu-id="d9ea3-217">A user can also save a choice as the default action for this medium by clicking the **Always do the selected action** box.</span></span> <span data-ttu-id="d9ea3-218">Depois que essa opção for feita, a caixa de diálogo não será mostrada novamente.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-218">Once this choice is made, the dialog is not shown again.</span></span> <span data-ttu-id="d9ea3-219">No entanto, no Windows XP Service Pack 1 (SP1), se um novo aplicativo que pode manipular um determinado tipo de mídia for adicionado ao computador, a caixa de diálogo será novamente apresentada ao usuário, dando a oportunidade de selecionar o novo aplicativo como a ação de reprodução automática padrão.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-219">However, in Windows XP Service Pack 1 (SP1), if a new application that can handle a particular media type is added to the computer, the dialog is once again presented to the user, giving them the opportunity to select the new application as the default AutoPlay action.</span></span> <span data-ttu-id="d9ea3-220">Os aplicativos também podem ser definidos como a seleção padrão quando são instalados.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-220">Applications can also set themselves as the default selection when they are installed.</span></span>

<span data-ttu-id="d9ea3-221">O Windows XP SP1 também adiciona um recurso que retém a opção de ação de reprodução automática do usuário se eles não clicarem na caixa de **ação sempre fazer a seleção** .</span><span class="sxs-lookup"><span data-stu-id="d9ea3-221">Windows XP SP1 also adds a feature that retains the user's choice of AutoPlay action if they do not click the **Always do the selected action** box.</span></span> <span data-ttu-id="d9ea3-222">Se um usuário escolher uma ação de reprodução automática para uma única instância, na próxima vez que essa caixa de diálogo for apresentada para esse tipo de mídia, a mesma ação será a seleção padrão.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-222">If a user chooses an AutoPlay action for a single instance, the next time that dialog is presented for that media type, the same action is the default selection.</span></span>

<span data-ttu-id="d9ea3-223">Para que um aplicativo seja incluído na lista de ações possíveis, ele deve ser registrado com a reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-223">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="d9ea3-224">Para obter mais informações, consulte [preparando o hardware e o software para uso com a reprodução automática](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-224">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="mixed-media-dialog-box"></a><span data-ttu-id="d9ea3-225">Caixa de diálogo mídia mista</span><span class="sxs-lookup"><span data-stu-id="d9ea3-225">Mixed Media Dialog Box</span></span>

<span data-ttu-id="d9ea3-226">A caixa de diálogo a seguir é exibida quando qualquer meio contendo uma combinação de tipos de arquivo com suporte é apresentada ao sistema.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-226">The following dialog box is displayed when any medium containing a mix of supported file types is presented to the system.</span></span> <span data-ttu-id="d9ea3-227">Isso é essencialmente o mesmo que a caixa de diálogo meio de conteúdo único, mas com duas diferenças significativas.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-227">This is essentially the same as the single content medium dialog box but with two significant differences.</span></span> <span data-ttu-id="d9ea3-228">Primeiro, as opções de ação disponíveis consistem em uma lista filtrada de aplicativos relevantes para todos os tipos de conteúdo presentes na mídia.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-228">First, the available action options consist of a filtered list of applications relevant to all content types present on the medium.</span></span> <span data-ttu-id="d9ea3-229">Em segundo lugar, não há nenhuma opção para escolher uma ação padrão permanente, pois os tipos de conteúdo e as porcentagens de mídia de conteúdo mista são muito imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-229">Second, there is no option to choose a permanent default action because the content types and percentages of mixed content media are too unpredictable.</span></span>

![captura de tela da caixa de diálogo mídia mista](images/mix.png)

<span data-ttu-id="d9ea3-231">Para que um aplicativo seja incluído na lista de ações possíveis, ele deve ser registrado com a reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-231">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="d9ea3-232">Para obter mais informações, consulte [preparando o hardware e o software para uso com a reprodução automática](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="d9ea3-232">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="property-page"></a><span data-ttu-id="d9ea3-233">Página de Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9ea3-233">Property Page</span></span>

<span data-ttu-id="d9ea3-234">Veja a seguir uma página de propriedades de reprodução automática de exemplo para um dispositivo de DVD/CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-234">The following is a sample AutoPlay property page for a DVD/CD-ROM device.</span></span>

![captura de tela da página de propriedades](images/apdlg.png)

<span data-ttu-id="d9ea3-236">Cada tipo de dispositivo oferece um subconjunto apropriado de tipos de conteúdo para configuração de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-236">Each device type offers an appropriate subset of content types for AutoPlay configuration.</span></span> <span data-ttu-id="d9ea3-237">Por sua vez, cada tipo de conteúdo, quando selecionado, oferece uma lista apropriada de opções de ação na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-237">In turn, each content type, when selected, offers an appropriate list of action options in the list box.</span></span> <span data-ttu-id="d9ea3-238">Uma ação diferente pode ser escolhida para cada tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d9ea3-238">A different action can be chosen for each content type.</span></span>

 

 



