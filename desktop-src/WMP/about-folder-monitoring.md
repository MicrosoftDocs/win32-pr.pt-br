---
title: Sobre o monitoramento de pastas
description: Sobre o monitoramento de pastas
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, monitoramento de pastas
- Modelo de objeto do Windows Media Player, monitoramento de pastas
- modelo de objeto, monitoramento de pasta
- Controle ActiveX do Windows Media Player, monitoramento de pastas
- Controle ActiveX, monitoramento de pastas
- Controle ActiveX móvel do Windows Media Player, monitoramento de pastas
- Windows Media Player Mobile, monitoramento de pasta
- monitoramento de pastas
- pastas de monitoramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365526"
---
# <a name="about-folder-monitoring"></a><span data-ttu-id="3d334-112">Sobre o monitoramento de pastas</span><span class="sxs-lookup"><span data-stu-id="3d334-112">About Folder Monitoring</span></span>

<span data-ttu-id="3d334-113">O Windows Media Player pode monitorar pastas que contêm arquivos de mídia digital e atualizar a biblioteca quando os arquivos são adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="3d334-113">Windows Media Player can monitor folders that contain digital media files and update the library when files are added or removed.</span></span> <span data-ttu-id="3d334-114">Essa funcionalidade de monitoramento de pasta é fornecida pela interface [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) .</span><span class="sxs-lookup"><span data-stu-id="3d334-114">This folder monitoring functionality is provided by the [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) interface.</span></span>

<span data-ttu-id="3d334-115">Para usar os serviços de monitoramento de pasta, você deve criar o objeto do Player em um estado remoto.</span><span class="sxs-lookup"><span data-stu-id="3d334-115">To use the folder monitoring services, you must create the Player object in a remote state.</span></span> <span data-ttu-id="3d334-116">Para obter mais informações sobre comunicação remota, consulte [comunicação remota do controle do Windows Media Player](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="3d334-116">For more information about remoting, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span> <span data-ttu-id="3d334-117">Depois de criar uma instância remota do Player, obtenha um ponteiro para a interface **IWMPFolderMonitorServices** chamando **QueryInterface** na interface [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .</span><span class="sxs-lookup"><span data-stu-id="3d334-117">After you have created a remoted instance of the player, obtain a pointer to the **IWMPFolderMonitorServices** interface by calling **QueryInterface** on the [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) interface.</span></span>

<span data-ttu-id="3d334-118">O Windows Media Player mantém uma lista de pastas que estão sendo monitoradas.</span><span class="sxs-lookup"><span data-stu-id="3d334-118">Windows Media Player keeps a list of folders that are being monitored.</span></span> <span data-ttu-id="3d334-119">Para obter uma lista de pastas monitoradas, use os métodos [IWMPFolderMonitorServices:: get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) e [IWMPFolderMonitorServices:: item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) .</span><span class="sxs-lookup"><span data-stu-id="3d334-119">To get a list of monitored folders, use the [IWMPFolderMonitorServices::get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) and [IWMPFolderMonitorServices::item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) methods.</span></span> <span data-ttu-id="3d334-120">Para adicionar pastas à lista ou removê-las da lista, use os métodos [IWMPFolderMonitorServices:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) e [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3d334-120">To add folders to the list or remove them from the list, use the [IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) and [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) methods, respectively.</span></span>

<span data-ttu-id="3d334-121">**Iniciando uma verificação**</span><span class="sxs-lookup"><span data-stu-id="3d334-121">**Starting a Scan**</span></span>

<span data-ttu-id="3d334-122">O monitoramento de pastas normalmente é um processo em segundo plano que não precisa ser chamado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="3d334-122">Monitoring of folders is normally a background process that does not need to be called explicitly.</span></span> <span data-ttu-id="3d334-123">Se você quiser examinar ativamente uma pasta, chame [IWMPFolderMonitorServices:: startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span><span class="sxs-lookup"><span data-stu-id="3d334-123">If you want to actively scan a folder, call [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span></span> <span data-ttu-id="3d334-124">Você pode interromper uma verificação em andamento com o método [IWMPFolderMonitorServices:: stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .</span><span class="sxs-lookup"><span data-stu-id="3d334-124">You can stop a scan in progress with the [IWMPFolderMonitorServices::stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) method.</span></span>

<span data-ttu-id="3d334-125">**Recuperando o status de monitoramento da pasta**</span><span class="sxs-lookup"><span data-stu-id="3d334-125">**Retrieving the Folder Monitoring Status**</span></span>

<span data-ttu-id="3d334-126">O **IWMPFolderMonitorServices** fornece a funcionalidade para recuperar o status do processo de monitoramento de pasta.</span><span class="sxs-lookup"><span data-stu-id="3d334-126">**IWMPFolderMonitorServices** provides functionality for retrieving the status of the folder monitoring process.</span></span>

<span data-ttu-id="3d334-127">A verificação de pasta é feita em duas passagens.</span><span class="sxs-lookup"><span data-stu-id="3d334-127">Folder scanning is done in two passes.</span></span> <span data-ttu-id="3d334-128">Na primeira passagem, o Player examina as pastas nomeadas na lista pastas monitoradas uma por uma e cria uma lista de arquivos a serem adicionados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3d334-128">In the first pass, the Player scans the folders named in the monitored folders list one by one and builds a list of files to be added to the library.</span></span> <span data-ttu-id="3d334-129">Na segunda passagem, ele passa pela lista de arquivos e adiciona os arquivos à biblioteca e também remove todos os itens de mídia da biblioteca cujos arquivos físicos correspondentes foram excluídos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3d334-129">In the second pass, it goes through the list of files and adds the files to the library, and also removes any media items from the library whose corresponding physical files have been deleted from the file system.</span></span>

<span data-ttu-id="3d334-130">O evento [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) é usado para notificar seu programa sempre que o jogador alternar para um novo estado.</span><span class="sxs-lookup"><span data-stu-id="3d334-130">The [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) event is used to notify your program whenever the Player switches to a new state.</span></span> <span data-ttu-id="3d334-131">Você também pode recuperar o estado atual chamando [Get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span><span class="sxs-lookup"><span data-stu-id="3d334-131">You can also retrieve the current state by calling [get\_scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span></span> <span data-ttu-id="3d334-132">Quando a primeira passagem é iniciada, o valor do estado atual é wmpfssScanning.</span><span class="sxs-lookup"><span data-stu-id="3d334-132">When the first pass starts, the current state value is wmpfssScanning.</span></span> <span data-ttu-id="3d334-133">Durante a segunda passagem, o estado muda para wmpfssUpdating.</span><span class="sxs-lookup"><span data-stu-id="3d334-133">During the second pass, the state switches to wmpfssUpdating.</span></span> <span data-ttu-id="3d334-134">Depois que o processo for concluído, o estado será alterado para wmpfssStopped.</span><span class="sxs-lookup"><span data-stu-id="3d334-134">After the process is finished, the state changes to wmpfssStopped.</span></span>

<span data-ttu-id="3d334-135">Enquanto o Player estiver verificando as pastas monitoradas na primeira passagem, chame [Get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) para verificar quantos arquivos foram verificados.</span><span class="sxs-lookup"><span data-stu-id="3d334-135">While the Player is scanning the monitored folders on the first pass, call [get\_scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) to check how many files have been scanned.</span></span> <span data-ttu-id="3d334-136">O método [Get \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) informará qual pasta está sendo verificada no momento.</span><span class="sxs-lookup"><span data-stu-id="3d334-136">The [get\_currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) method will tell you which folder is currently being scanned.</span></span>

<span data-ttu-id="3d334-137">Depois que a segunda passagem for iniciada, chame [Get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) para verificar quantos arquivos foram adicionados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3d334-137">After the second pass starts, call [get\_addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) to check how many files have been added to the library.</span></span> <span data-ttu-id="3d334-138">O método [Get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) informará o progresso da segunda passagem, como uma porcentagem de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="3d334-138">The [get\_updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) method will tell you the progress of the second pass, as a percentage from 0 to 100.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d334-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d334-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d334-140">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="3d334-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="3d334-141">**Interface IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="3d334-141">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




