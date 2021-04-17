---
title: Interface IWMPNetwork (VB e C) (WMP. h)
description: Fornece propriedades e métodos para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede. A interface IWMPNetwork expõe as propriedades a seguir.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- IWMPNetwork (VB e C) interface do Windows Media Player
- IWMPNetwork (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780220"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a><span data-ttu-id="1e3d1-105">Interface IWMPNetwork (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="1e3d1-105">IWMPNetwork (VB and C#) interface</span></span>

<span data-ttu-id="1e3d1-106">Fornece propriedades e métodos para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-106">Provides properties and methods to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="1e3d1-107">A interface **IWMPNetwork** expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-107">The **IWMPNetwork** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="1e3d1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1e3d1-108">Members</span></span>

<span data-ttu-id="1e3d1-109">A interface **IWMPNetwork (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1e3d1-109">The **IWMPNetwork (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="1e3d1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e3d1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1e3d1-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e3d1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1e3d1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e3d1-112">Methods</span></span>

<span data-ttu-id="1e3d1-113">A interface **IWMPNetwork (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-113">The **IWMPNetwork (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="1e3d1-114">Método</span><span class="sxs-lookup"><span data-stu-id="1e3d1-114">Method</span></span>                                                                                           | <span data-ttu-id="1e3d1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e3d1-115">Description</span></span>                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e3d1-116">**getProxyBypassForLocal**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-116">**getProxyBypassForLocal**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | <span data-ttu-id="1e3d1-117">Retorna um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-117">Returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/> |
| [<span data-ttu-id="1e3d1-118">**getProxyExceptionList**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-118">**getProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="1e3d1-119">Retorna a lista de exceções de proxy.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-119">Returns the proxy exception list.</span></span><br/>                                                                           |
| [<span data-ttu-id="1e3d1-120">**getproxyname**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-120">**getProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | <span data-ttu-id="1e3d1-121">Retorna o nome do servidor proxy que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-121">Returns the name of the proxy server being used.</span></span><br/>                                                            |
| [<span data-ttu-id="1e3d1-122">**getProxyPort**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-122">**getProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | <span data-ttu-id="1e3d1-123">Retorna a porta do proxy que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-123">Returns the proxy port being used.</span></span><br/>                                                                          |
| [<span data-ttu-id="1e3d1-124">**getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-124">**getProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | <span data-ttu-id="1e3d1-125">Retorna informações sobre as configurações de proxy para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-125">Returns information about the proxy settings for a protocol.</span></span><br/>                                                |
| [<span data-ttu-id="1e3d1-126">**setProxyBypassForLocal**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-126">**setProxyBypassForLocal**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | <span data-ttu-id="1e3d1-127">Especifica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-127">Specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/>                  |
| [<span data-ttu-id="1e3d1-128">**setProxyExceptionList**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-128">**setProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="1e3d1-129">Especifica a lista de exceções de proxy.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-129">Specifies the proxy exception list.</span></span><br/>                                                                         |
| [<span data-ttu-id="1e3d1-130">**setproxyname**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-130">**setProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | <span data-ttu-id="1e3d1-131">Especifica o nome do servidor proxy a ser usado.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-131">Specifies the name of the proxy server to use.</span></span><br/>                                                              |
| [<span data-ttu-id="1e3d1-132">**setProxyPort**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-132">**setProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | <span data-ttu-id="1e3d1-133">Especifica a porta proxy a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-133">Specifies the proxy port to use.</span></span><br/>                                                                            |
| [<span data-ttu-id="1e3d1-134">**setProxySettings**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-134">**setProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | <span data-ttu-id="1e3d1-135">Especifica as configurações de proxy para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-135">Specifies the proxy settings for a protocol.</span></span><br/>                                                                |



 

### <a name="properties"></a><span data-ttu-id="1e3d1-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e3d1-136">Properties</span></span>

<span data-ttu-id="1e3d1-137">A interface **IWMPNetwork (VB e C#)** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-137">The **IWMPNetwork (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="1e3d1-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1e3d1-138">Property</span></span>                                                                                          | <span data-ttu-id="1e3d1-139">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="1e3d1-139">Access type</span></span>           | <span data-ttu-id="1e3d1-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e3d1-140">Description</span></span>                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e3d1-141">**Larga**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-141">**bandWidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | <span data-ttu-id="1e3d1-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-142">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-143">Obtém a largura de banda atual do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-143">Gets the current bandwidth of the media item.</span></span><br/>                                     |
| [<span data-ttu-id="1e3d1-144">**720p**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-144">**bitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | <span data-ttu-id="1e3d1-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-145">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-146">Obtém a taxa de bits atual sendo recebida.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-146">Gets the current bit rate being received.</span></span><br/>                                         |
| [<span data-ttu-id="1e3d1-147">**bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-147">**bufferingCount**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | <span data-ttu-id="1e3d1-148">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-148">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-149">Obtém o número de vezes que o buffer ocorreu durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-149">Gets the number of times buffering occurred during playback.</span></span><br/>                      |
| [<span data-ttu-id="1e3d1-150">**bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-150">**bufferingProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | <span data-ttu-id="1e3d1-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-151">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-152">Obtém a porcentagem de buffer concluído.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-152">Gets the percentage of buffering completed.</span></span><br/>                                       |
| [<span data-ttu-id="1e3d1-153">**bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-153">**bufferingTime**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | <span data-ttu-id="1e3d1-154">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1e3d1-154">Read/write</span></span><br/> | <span data-ttu-id="1e3d1-155">Obtém ou define a quantidade de tempo de buffer em milissegundos antes que a reprodução seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-155">Gets or sets the amount of buffering time in milliseconds before playback begins.</span></span><br/> |
| [<span data-ttu-id="1e3d1-156">**downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-156">**downloadProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | <span data-ttu-id="1e3d1-157">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-157">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-158">Obtém a porcentagem de download concluído.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-158">Gets the percentage of downloading completed.</span></span><br/>                                     |
| [<span data-ttu-id="1e3d1-159">**encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-159">**encodedFrameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | <span data-ttu-id="1e3d1-160">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-160">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-161">Obtém a taxa de quadros de vídeo especificada pelo autor do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-161">Gets the video frame rate specified by the content author.</span></span><br/>                        |
| [<span data-ttu-id="1e3d1-162">**Quadros**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-162">**frameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | <span data-ttu-id="1e3d1-163">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-163">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-164">Obtém a taxa de quadros de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-164">Gets the current video frame rate.</span></span><br/>                                                |
| [<span data-ttu-id="1e3d1-165">**framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-165">**framesSkipped**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | <span data-ttu-id="1e3d1-166">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-166">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-167">Obtém o número total de quadros ignorados durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-167">Gets the total number of frames skipped during playback.</span></span><br/>                          |
| [<span data-ttu-id="1e3d1-168">**lostPackets**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-168">**lostPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | <span data-ttu-id="1e3d1-169">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-169">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-170">Obtém o número de pacotes perdidos.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-170">Gets the number of packets lost.</span></span><br/>                                                  |
| [<span data-ttu-id="1e3d1-171">**maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-171">**maxBandwidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | <span data-ttu-id="1e3d1-172">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1e3d1-172">Read/write</span></span><br/> | <span data-ttu-id="1e3d1-173">Obtém ou define a largura de banda máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-173">Gets or sets the maximum allowed bandwidth.</span></span><br/>                                       |
| [<span data-ttu-id="1e3d1-174">**maxBitRate**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-174">**maxBitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | <span data-ttu-id="1e3d1-175">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-175">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-176">Obtém a taxa máxima de bits de vídeo possível.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-176">Gets the maximum possible video bit rate.</span></span><br/>                                         |
| [<span data-ttu-id="1e3d1-177">**receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-177">**receivedPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | <span data-ttu-id="1e3d1-178">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-178">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-179">Obtém o número de pacotes recebidos.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-179">Gets the number of packets received.</span></span><br/>                                              |
| [<span data-ttu-id="1e3d1-180">**receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-180">**receptionQuality**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | <span data-ttu-id="1e3d1-181">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-181">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-182">Obtém a porcentagem de pacotes que não são perdidos nos últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-182">Gets the percentage of packets not lost in the last 30 seconds.</span></span><br/>                   |
| [<span data-ttu-id="1e3d1-183">**recoveredPackets**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-183">**recoveredPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | <span data-ttu-id="1e3d1-184">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-184">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-185">Obtém o número de pacotes recuperados.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-185">Gets the number of recovered packets.</span></span><br/>                                             |
| [<span data-ttu-id="1e3d1-186">**sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-186">**sourceProtocol**</span></span>](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | <span data-ttu-id="1e3d1-187">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e3d1-187">Read-only</span></span><br/>  | <span data-ttu-id="1e3d1-188">Obtém o protocolo de origem usado para receber dados.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-188">Gets the source protocol used to receive data.</span></span><br/>                                    |



 

<span data-ttu-id="1e3d1-189">Obtenha uma interface **IWMPNetwork** usando a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-189">Get an **IWMPNetwork** interface by using the following property.</span></span>



| <span data-ttu-id="1e3d1-190">Objeto</span><span class="sxs-lookup"><span data-stu-id="1e3d1-190">Object</span></span>                                                                   | <span data-ttu-id="1e3d1-191">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1e3d1-191">Property</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="1e3d1-192">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="1e3d1-192">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="1e3d1-193">**rede**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-193">**network**</span></span>](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="1e3d1-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e3d1-194">Requirements</span></span>



| <span data-ttu-id="1e3d1-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e3d1-195">Requirement</span></span> | <span data-ttu-id="1e3d1-196">Valor</span><span class="sxs-lookup"><span data-stu-id="1e3d1-196">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1e3d1-197">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e3d1-197">Header</span></span><br/> | <dl> <span data-ttu-id="1e3d1-198"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e3d1-198"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e3d1-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e3d1-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e3d1-200">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="1e3d1-200">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





