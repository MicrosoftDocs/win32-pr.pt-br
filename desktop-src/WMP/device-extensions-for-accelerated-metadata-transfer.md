---
title: Extensões de dispositivo para transferência de metadados acelerada
description: Extensões de dispositivo para transferência de metadados acelerada
ms.assetid: a79b54d4-dad5-411b-aaff-b58bb549d4d1
keywords:
- Windows Media Player, extensões de dispositivo
- Windows Media Player, extensões
- Windows Media Player, transferência de metadados acelerada
- Windows Media Player, transferência acelerada de metadados
- transferência de metadados acelerada
- metadados, transferência acelerada
- extensões de dispositivo, transferência de metadados acelerada
- extensões, transferência de metadados acelerada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe661dff0750f2ad46bef96e537b0852d480db8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005769"
---
# <a name="device-extensions-for-accelerated-metadata-transfer"></a><span data-ttu-id="34059-111">Extensões de dispositivo para transferência de metadados acelerada</span><span class="sxs-lookup"><span data-stu-id="34059-111">Device Extensions for Accelerated Metadata Transfer</span></span>

<span data-ttu-id="34059-112">O Windows Media Player 10 introduziu funcionalidades novas e estendidas para sincronizar arquivos de mídia digital com dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="34059-112">Windows Media Player 10 introduced new and extended functionality for synchronizing digital media files with portable devices.</span></span> <span data-ttu-id="34059-113">Os usuários podem conectar um dispositivo a um computador, transferir conteúdo para o dispositivo e, em seguida, desconectar o dispositivo para desfrutar do conteúdo do computador.</span><span class="sxs-lookup"><span data-stu-id="34059-113">Users can connect a device to a computer, transfer content to the device, and then disconnect the device to enjoy content away from the computer.</span></span>

<span data-ttu-id="34059-114">Quando o usuário reconecta o dispositivo ao computador, é possível que o conteúdo armazenado no dispositivo seja alterado desde a conexão anterior.</span><span class="sxs-lookup"><span data-stu-id="34059-114">When the user reconnects the device to the computer, it is possible that the content stored on the device changed since the previous connection.</span></span> <span data-ttu-id="34059-115">Por exemplo, a simples reprodução de um arquivo de mídia digital específico faz com que a contagem de reprodução desse item seja alterada.</span><span class="sxs-lookup"><span data-stu-id="34059-115">For example, simply playing a particular digital media file causes the play count for that item to change.</span></span> <span data-ttu-id="34059-116">Como os dispositivos portáteis atuais podem armazenar grandes quantidades de conteúdo de mídia digital, o processo de descoberta de alterações seria muito demorado se o Windows Media Player fosse solicitado a enumerar e inspecionar cada item de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="34059-116">Because current portable devices can store large quantities of digital media content, the process of discovering changes would be too time consuming if Windows Media Player were required to enumerate and inspect each digital media item.</span></span> <span data-ttu-id="34059-117">Em vez disso, os fabricantes de dispositivos portáteis podem implementar uma funcionalidade especial para habilitar o Windows Media Player 10 ou posterior para recuperar com eficiência as informações sobre as alterações feitas no conteúdo armazenado em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34059-117">Instead, portable device manufacturers can implement special functionality to enable Windows Media Player 10 or later to efficiently retrieve information about changes made to the content stored on a device.</span></span>

<span data-ttu-id="34059-118">As seções a seguir descrevem as convenções usadas para implementar essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="34059-118">The following sections describe the conventions used to implement this functionality.</span></span>

-   [<span data-ttu-id="34059-119">Sobre os metadados</span><span class="sxs-lookup"><span data-stu-id="34059-119">About the Metadata</span></span>](about-the-metadata.md)
-   [<span data-ttu-id="34059-120">Extensões de dispositivo MTP para transferência de metadados</span><span class="sxs-lookup"><span data-stu-id="34059-120">MTP Device Extensions for Metadata Transfer</span></span>](mtp-device-extensions-for-metadata-transfer.md)
-   [<span data-ttu-id="34059-121">Extensões de dispositivo do Windows Media Gerenciador de Dispositivos para transferência de metadados</span><span class="sxs-lookup"><span data-stu-id="34059-121">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>](windows-media-device-manager-device-extensions-for-metadata-transfer.md)

## <a name="related-topics"></a><span data-ttu-id="34059-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34059-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34059-123">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="34059-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




