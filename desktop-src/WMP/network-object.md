---
title: Objeto de rede
description: O objeto de rede fornece propriedades e métodos usados para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Objeto de rede Windows Media Player
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104365065"
---
# <a name="network-object"></a><span data-ttu-id="dc7b0-104">Objeto de rede</span><span class="sxs-lookup"><span data-stu-id="dc7b0-104">Network Object</span></span>

<span data-ttu-id="dc7b0-105">O objeto de **rede** fornece propriedades e métodos usados para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-105">The **Network** object provides properties and methods used to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="dc7b0-106">O objeto de **rede** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-106">The **Network** object supports the following properties.</span></span>



| <span data-ttu-id="dc7b0-107">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dc7b0-107">Property</span></span>                                           | <span data-ttu-id="dc7b0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc7b0-108">Description</span></span>                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc7b0-109">Larga</span><span class="sxs-lookup"><span data-stu-id="dc7b0-109">bandWidth</span></span>](network-bandwidth.md)                 | <span data-ttu-id="dc7b0-110">Recupera a largura de banda atual do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-110">Retrieves the current bandwidth of the media item.</span></span>                                          |
| [<span data-ttu-id="dc7b0-111">720p</span><span class="sxs-lookup"><span data-stu-id="dc7b0-111">bitRate</span></span>](network-bitrate.md)                     | <span data-ttu-id="dc7b0-112">Recupera a taxa de bits atual que está sendo recebida.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-112">Retrieves the current bit rate being received.</span></span>                                              |
| [<span data-ttu-id="dc7b0-113">bufferingCount</span><span class="sxs-lookup"><span data-stu-id="dc7b0-113">bufferingCount</span></span>](network-bufferingcount.md)       | <span data-ttu-id="dc7b0-114">Recupera o número de vezes que o buffer ocorreu durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-114">Retrieves the number of times buffering occurred during playback.</span></span>                           |
| [<span data-ttu-id="dc7b0-115">bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="dc7b0-115">bufferingProgress</span></span>](network-bufferingprogress.md) | <span data-ttu-id="dc7b0-116">Recupera a porcentagem de buffer concluído.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-116">Retrieves the percentage of buffering completed.</span></span>                                            |
| [<span data-ttu-id="dc7b0-117">bufferingTime</span><span class="sxs-lookup"><span data-stu-id="dc7b0-117">bufferingTime</span></span>](network-bufferingtime.md)         | <span data-ttu-id="dc7b0-118">Especifica ou recupera a quantidade de tempo de buffer em milissegundos antes que a reprodução seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-118">Specifies or retrieves the amount of buffering time in milliseconds before playback begins.</span></span> |
| [<span data-ttu-id="dc7b0-119">downloadProgress</span><span class="sxs-lookup"><span data-stu-id="dc7b0-119">downloadProgress</span></span>](network-downloadprogress.md)   | <span data-ttu-id="dc7b0-120">Recupera o percentual de download concluído.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-120">Retrieves the percentage of download completed.</span></span>                                             |
| [<span data-ttu-id="dc7b0-121">encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="dc7b0-121">encodedFrameRate</span></span>](network-encodedframerate.md)   | <span data-ttu-id="dc7b0-122">Recupera a taxa de quadros de vídeo especificada pelo autor do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-122">Retrieves the video frame rate specified by the content author.</span></span>                             |
| [<span data-ttu-id="dc7b0-123">Quadros</span><span class="sxs-lookup"><span data-stu-id="dc7b0-123">frameRate</span></span>](network-framerate.md)                 | <span data-ttu-id="dc7b0-124">Recupera a taxa de quadros de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-124">Retrieves the current video frame rate.</span></span>                                                     |
| [<span data-ttu-id="dc7b0-125">framesSkipped</span><span class="sxs-lookup"><span data-stu-id="dc7b0-125">framesSkipped</span></span>](network-framesskipped.md)         | <span data-ttu-id="dc7b0-126">Recupera o número total de quadros ignorados durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-126">Retrieves the total number of frames skipped during playback.</span></span>                               |
| [<span data-ttu-id="dc7b0-127">lostPackets</span><span class="sxs-lookup"><span data-stu-id="dc7b0-127">lostPackets</span></span>](network-lostpackets.md)             | <span data-ttu-id="dc7b0-128">Recupera o número de pacotes perdidos.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-128">Retrieves the number of packets lost.</span></span>                                                       |
| [<span data-ttu-id="dc7b0-129">maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="dc7b0-129">maxBandwidth</span></span>](network-maxbandwidth.md)           | <span data-ttu-id="dc7b0-130">Especifica ou recupera a largura de banda máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-130">Specifies or retrieves the maximum allowed bandwidth.</span></span>                                       |
| [<span data-ttu-id="dc7b0-131">maxBitRate</span><span class="sxs-lookup"><span data-stu-id="dc7b0-131">maxBitRate</span></span>](network-maxbitrate.md)               | <span data-ttu-id="dc7b0-132">Recupera a taxa máxima de bits de vídeo possível.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-132">Retrieves the maximum possible video bit rate.</span></span>                                              |
| [<span data-ttu-id="dc7b0-133">receivedPackets</span><span class="sxs-lookup"><span data-stu-id="dc7b0-133">receivedPackets</span></span>](network-receivedpackets.md)     | <span data-ttu-id="dc7b0-134">Recupera o número de pacotes recebidos.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-134">Retrieves the number of packets received.</span></span>                                                   |
| [<span data-ttu-id="dc7b0-135">receptionQuality</span><span class="sxs-lookup"><span data-stu-id="dc7b0-135">receptionQuality</span></span>](network-receptionquality.md)   | <span data-ttu-id="dc7b0-136">Recupera a porcentagem de pacotes recebidos nos últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-136">Retrieves the percentage of packets received in the last 30 seconds.</span></span>                        |
| [<span data-ttu-id="dc7b0-137">recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="dc7b0-137">recoveredPackets</span></span>](network-recoveredpackets.md)   | <span data-ttu-id="dc7b0-138">Recupera o número de pacotes recuperados.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-138">Retrieves the number of recovered packets.</span></span>                                                  |
| [<span data-ttu-id="dc7b0-139">sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="dc7b0-139">sourceProtocol</span></span>](network-sourceprotocol.md)       | <span data-ttu-id="dc7b0-140">Recupera o protocolo de origem usado para receber dados.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-140">Retrieves the source protocol used to receive data.</span></span>                                         |



 

<span data-ttu-id="dc7b0-141">O objeto de **rede** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-141">The **Network** object supports the following methods.</span></span>



| <span data-ttu-id="dc7b0-142">Método</span><span class="sxs-lookup"><span data-stu-id="dc7b0-142">Method</span></span>                                                       | <span data-ttu-id="dc7b0-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc7b0-143">Description</span></span>                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc7b0-144">getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="dc7b0-144">getProxyBypassForLocal</span></span>](network-getproxybypassforlocal.md) | <span data-ttu-id="dc7b0-145">Recupera um valor que indica se o servidor proxy deve ser ignorado se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-145">Retrieves a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="dc7b0-146">getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="dc7b0-146">getProxyExceptionList</span></span>](network-getproxyexceptionlist.md)   | <span data-ttu-id="dc7b0-147">Recupera a lista de exceções de proxy.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-147">Retrieves the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="dc7b0-148">getproxyname</span><span class="sxs-lookup"><span data-stu-id="dc7b0-148">getProxyName</span></span>](network-getproxyname.md)                     | <span data-ttu-id="dc7b0-149">Recupera o nome de um servidor proxy a ser usado.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-149">Retrieves the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="dc7b0-150">getProxyPort</span><span class="sxs-lookup"><span data-stu-id="dc7b0-150">getProxyPort</span></span>](network-getproxyport.md)                     | <span data-ttu-id="dc7b0-151">Recupera a porta proxy a ser usada.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-151">Retrieves the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="dc7b0-152">getProxySettings</span><span class="sxs-lookup"><span data-stu-id="dc7b0-152">getProxySettings</span></span>](network-getproxysettings.md)             | <span data-ttu-id="dc7b0-153">Recupera a configuração de proxy para um determinado protocolo.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-153">Retrieves the proxy setting for a given protocol.</span></span>                                                                    |
| [<span data-ttu-id="dc7b0-154">setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="dc7b0-154">setProxyBypassForLocal</span></span>](network-setproxybypassforlocal.md) | <span data-ttu-id="dc7b0-155">Especifica um valor que indica se o servidor proxy deve ser ignorado se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-155">Specifies a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="dc7b0-156">setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="dc7b0-156">setProxyExceptionList</span></span>](network-setproxyexceptionlist.md)   | <span data-ttu-id="dc7b0-157">Especifica a lista de exceções de proxy.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-157">Specifies the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="dc7b0-158">setproxyname</span><span class="sxs-lookup"><span data-stu-id="dc7b0-158">setProxyName</span></span>](network-setproxyname.md)                     | <span data-ttu-id="dc7b0-159">Especifica o nome de um servidor proxy a ser usado.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-159">Specifies the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="dc7b0-160">setProxyPort</span><span class="sxs-lookup"><span data-stu-id="dc7b0-160">setProxyPort</span></span>](network-setproxyport.md)                     | <span data-ttu-id="dc7b0-161">Especifica a porta proxy a ser usada.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-161">Specifies the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="dc7b0-162">setProxySettings</span><span class="sxs-lookup"><span data-stu-id="dc7b0-162">setProxySettings</span></span>](network-setproxysettings.md)             | <span data-ttu-id="dc7b0-163">Especifica a configuração de proxy para um determinado protocolo.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-163">Specifies the proxy setting for a given protocol.</span></span>                                                                    |



 

<span data-ttu-id="dc7b0-164">O objeto de **rede** é acessado por meio da propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc7b0-164">The **Network** object is accessed through the following property.</span></span>



| <span data-ttu-id="dc7b0-165">Objeto</span><span class="sxs-lookup"><span data-stu-id="dc7b0-165">Object</span></span>                      | <span data-ttu-id="dc7b0-166">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dc7b0-166">Property</span></span>                      |
|-----------------------------|-------------------------------|
| [<span data-ttu-id="dc7b0-167">Jogador</span><span class="sxs-lookup"><span data-stu-id="dc7b0-167">Player</span></span>](player-object.md) | [<span data-ttu-id="dc7b0-168">rede</span><span class="sxs-lookup"><span data-stu-id="dc7b0-168">network</span></span>](player-network.md) |



 

## <a name="see-also"></a><span data-ttu-id="dc7b0-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc7b0-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7b0-170">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="dc7b0-170">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




