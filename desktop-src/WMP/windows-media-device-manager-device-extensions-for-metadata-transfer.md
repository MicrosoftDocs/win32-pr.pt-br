---
title: Extensões de dispositivo do Windows Media Gerenciador de Dispositivos para transferência de metadados
description: Extensões de dispositivo do Windows Media Gerenciador de Dispositivos para transferência de metadados
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, extensões de dispositivo
- Windows Media Player, extensões
- Windows Media Player, metadados
- Windows Media Player, transferência de metadados acelerada
- Windows Media Player, transferência acelerada de metadados
- metadados, extensões de dispositivo
- metadados, extensões
- extensões de dispositivo, transferência de metadados
- extensões, transferência de metadados
- transferência de metadados acelerada
- metadados, transferência acelerada
- extensões de dispositivo, transferência de metadados acelerada
- extensões, transferência de metadados acelerada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453645"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a><span data-ttu-id="d987b-116">Extensões de dispositivo do Windows Media Gerenciador de Dispositivos para transferência de metadados</span><span class="sxs-lookup"><span data-stu-id="d987b-116">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>

<span data-ttu-id="d987b-117">Para habilitar a transferência de metadados acelerada, os fabricantes de dispositivos que não dão suporte a MTP devem fazer o seguinte no código-fonte:</span><span class="sxs-lookup"><span data-stu-id="d987b-117">To enable accelerated metadata transfer, manufacturers of devices that do not support MTP must do the following in source code:</span></span>

-   <span data-ttu-id="d987b-118">Defina **o \_ \_ \_ suporte ao dispositivo WMDM do WMP**.</span><span class="sxs-lookup"><span data-stu-id="d987b-118">Define **WMP\_WMDM\_DEVICE\_SUPPORT**.</span></span>
-   <span data-ttu-id="d987b-119">Inclua wmpdevices. h, que é instalado como parte do SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d987b-119">Include wmpdevices.h, which is installed as part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="d987b-120">Wmpdevices. h define as estruturas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d987b-120">Wmpdevices.h defines the following structures.</span></span>



| <span data-ttu-id="d987b-121">Estrutura</span><span class="sxs-lookup"><span data-stu-id="d987b-121">Structure</span></span>                                                                                 | <span data-ttu-id="d987b-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="d987b-122">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d987b-123">\_PC2DEVICE de \_ \_ viagem de \_ ida \_ e volta de metadados do WMP</span><span class="sxs-lookup"><span data-stu-id="d987b-123">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | <span data-ttu-id="d987b-124">Estrutura usada pelo Windows Media Player para solicitar informações de sincronização de metadados aceleradas de dispositivos portáteis que não dão suporte a MTP.</span><span class="sxs-lookup"><span data-stu-id="d987b-124">Structure used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |
| [<span data-ttu-id="d987b-125">\_DEVICE2PC de \_ \_ viagem de \_ ida \_ e volta de metadados do WMP</span><span class="sxs-lookup"><span data-stu-id="d987b-125">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | <span data-ttu-id="d987b-126">Estrutura usada pelo Windows Media Player para receber informações de sincronização de metadados aceleradas de dispositivos portáteis que não dão suporte a MTP.</span><span class="sxs-lookup"><span data-stu-id="d987b-126">Structure used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |



 

<span data-ttu-id="d987b-127">Para solicitar informações do dispositivo sobre metadados que foram alterados, o Windows Media Player 10 ou posterior chama o método IWMDMDevice3 do Windows Media Gerenciador de Dispositivos **::D eviceiocontrol**.</span><span class="sxs-lookup"><span data-stu-id="d987b-127">To request information from the device about metadata that has changed, Windows Media Player 10 or later calls the Windows Media Device Manager method **IWMDMDevice3::DeviceIoControl**.</span></span> <span data-ttu-id="d987b-128">Ao fazer essa chamada, o Player segue etapas específicas, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d987b-128">When making this call, the Player follows specific steps, as follows:</span></span>

-   <span data-ttu-id="d987b-129">O primeiro parâmetro, *dwIoControlCode*, contém a viagem de ida e volta de metadados do WMP do **IOCTL \_ \_ \_ \_** constante.</span><span class="sxs-lookup"><span data-stu-id="d987b-129">The first parameter, *dwIoControlCode*, contains the constant **IOCTL\_WMP\_METADATA\_ROUND\_TRIP**.</span></span> <span data-ttu-id="d987b-130">Essa constante é definida em wmpdevices. h.</span><span class="sxs-lookup"><span data-stu-id="d987b-130">This constant is defined in wmpdevices.h.</span></span>
-   <span data-ttu-id="d987b-131">O segundo parâmetro, *lpInBuffer*, aponta para uma estrutura PC2DEVICE de viagem de ida e volta de **\_ \_ metadados \_ \_ \_ WMDM do WMP** .</span><span class="sxs-lookup"><span data-stu-id="d987b-131">The second parameter, *lpInBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE** structure.</span></span>
-   <span data-ttu-id="d987b-132">O terceiro parâmetro, *nInBufferSize*, contém o tamanho do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="d987b-132">The third parameter, *nInBufferSize*, contains the size of the input buffer.</span></span>
-   <span data-ttu-id="d987b-133">O quarto parâmetro, *lpOutBuffer*, aponta para uma estrutura DEVICE2PC de viagem de ida e volta de **\_ \_ metadados \_ \_ \_ WMDM do WMP** .</span><span class="sxs-lookup"><span data-stu-id="d987b-133">The fourth parameter, *lpOutBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC** structure.</span></span> <span data-ttu-id="d987b-134">O dispositivo deve preencher essa estrutura com informações sobre as alterações.</span><span class="sxs-lookup"><span data-stu-id="d987b-134">The device must fill in this structure with information about changes.</span></span>
-   <span data-ttu-id="d987b-135">O quinto parâmetro, *pnOutBufferSize*, recebe o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="d987b-135">The fifth parameter, *pnOutBufferSize*, receives the size of the output buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d987b-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d987b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d987b-137">**Extensões de dispositivo para transferência de metadados acelerada**</span><span class="sxs-lookup"><span data-stu-id="d987b-137">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




