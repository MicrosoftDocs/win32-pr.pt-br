---
title: Player. openState
description: A propriedade OpenState recupera um valor que indica o estado da fonte de conteúdo.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player. OpenState do Windows Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791518"
---
# <a name="playeropenstate"></a><span data-ttu-id="7f69e-104">Player. openState</span><span class="sxs-lookup"><span data-stu-id="7f69e-104">Player.openState</span></span>

<span data-ttu-id="7f69e-105">A propriedade **OpenState** recupera um valor que indica o estado da fonte de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7f69e-105">The **openState** property retrieves a value indicating the state of the content source.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f69e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f69e-106">Syntax</span></span>

<span data-ttu-id="7f69e-107">*Player* . **OpenState**</span><span class="sxs-lookup"><span data-stu-id="7f69e-107">*player* .**openState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7f69e-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7f69e-108">Possible Values</span></span>

<span data-ttu-id="7f69e-109">Essa propriedade é um **número** somente leitura (**longo**).</span><span class="sxs-lookup"><span data-stu-id="7f69e-109">This property is a read only **Number** (**long**).</span></span> <span data-ttu-id="7f69e-110">A constante de enumeração de estilo C pode ser derivada pela prefixação do valor de estado com "wmpos".</span><span class="sxs-lookup"><span data-stu-id="7f69e-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpos".</span></span> <span data-ttu-id="7f69e-111">Por exemplo, a constante para o estado PlaylistOpening é **wmposPlaylistOpening**.</span><span class="sxs-lookup"><span data-stu-id="7f69e-111">For example, the constant for the PlaylistOpening state is **wmposPlaylistOpening**.</span></span>



| <span data-ttu-id="7f69e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7f69e-112">Value</span></span> | <span data-ttu-id="7f69e-113">Estado</span><span class="sxs-lookup"><span data-stu-id="7f69e-113">State</span></span>                   | <span data-ttu-id="7f69e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f69e-114">Description</span></span>                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f69e-115">0</span><span class="sxs-lookup"><span data-stu-id="7f69e-115">0</span></span>     | <span data-ttu-id="7f69e-116">Indefinido</span><span class="sxs-lookup"><span data-stu-id="7f69e-116">Undefined</span></span>               | <span data-ttu-id="7f69e-117">O Windows Media Player está em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="7f69e-117">Windows Media Player is in an undefined state.</span></span>                                                                                                         |
| <span data-ttu-id="7f69e-118">1</span><span class="sxs-lookup"><span data-stu-id="7f69e-118">1</span></span>     | <span data-ttu-id="7f69e-119">PlaylistChanging</span><span class="sxs-lookup"><span data-stu-id="7f69e-119">PlaylistChanging</span></span>        | <span data-ttu-id="7f69e-120">A nova Playlist está prestes a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="7f69e-120">New playlist is about to be loaded.</span></span>                                                                                                                    |
| <span data-ttu-id="7f69e-121">2</span><span class="sxs-lookup"><span data-stu-id="7f69e-121">2</span></span>     | <span data-ttu-id="7f69e-122">PlaylistLocating</span><span class="sxs-lookup"><span data-stu-id="7f69e-122">PlaylistLocating</span></span>        | <span data-ttu-id="7f69e-123">O Windows Media Player está tentando localizar a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7f69e-123">Windows Media Player is attempting to locate the playlist.</span></span> <span data-ttu-id="7f69e-124">A lista de reprodução pode ser local (biblioteca ou metarquivo com uma extensão de nome de arquivo. asx) ou remoto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-124">The playlist can be local (library or metafile with an .asx file name extension) or remote.</span></span> |
| <span data-ttu-id="7f69e-125">3</span><span class="sxs-lookup"><span data-stu-id="7f69e-125">3</span></span>     | <span data-ttu-id="7f69e-126">PlaylistConnecting</span><span class="sxs-lookup"><span data-stu-id="7f69e-126">PlaylistConnecting</span></span>      | <span data-ttu-id="7f69e-127">Conectando-se à lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7f69e-127">Connecting to the playlist.</span></span>                                                                                                                            |
| <span data-ttu-id="7f69e-128">4</span><span class="sxs-lookup"><span data-stu-id="7f69e-128">4</span></span>     | <span data-ttu-id="7f69e-129">PlaylistLoading</span><span class="sxs-lookup"><span data-stu-id="7f69e-129">PlaylistLoading</span></span>         | <span data-ttu-id="7f69e-130">A playlist foi encontrada e agora está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="7f69e-130">Playlist has been found and is now being retrieved.</span></span>                                                                                                    |
| <span data-ttu-id="7f69e-131">5</span><span class="sxs-lookup"><span data-stu-id="7f69e-131">5</span></span>     | <span data-ttu-id="7f69e-132">PlaylistOpening</span><span class="sxs-lookup"><span data-stu-id="7f69e-132">PlaylistOpening</span></span>         | <span data-ttu-id="7f69e-133">A playlist foi recuperada e agora está sendo analisada e carregada.</span><span class="sxs-lookup"><span data-stu-id="7f69e-133">Playlist has been retrieved and is now being parsed and loaded.</span></span>                                                                                        |
| <span data-ttu-id="7f69e-134">6</span><span class="sxs-lookup"><span data-stu-id="7f69e-134">6</span></span>     | <span data-ttu-id="7f69e-135">PlaylistOpenNoMedia</span><span class="sxs-lookup"><span data-stu-id="7f69e-135">PlaylistOpenNoMedia</span></span>     | <span data-ttu-id="7f69e-136">A playlist está aberta.</span><span class="sxs-lookup"><span data-stu-id="7f69e-136">Playlist is open.</span></span>                                                                                                                                      |
| <span data-ttu-id="7f69e-137">7</span><span class="sxs-lookup"><span data-stu-id="7f69e-137">7</span></span>     | <span data-ttu-id="7f69e-138">Playlistchanged</span><span class="sxs-lookup"><span data-stu-id="7f69e-138">PlaylistChanged</span></span>         | <span data-ttu-id="7f69e-139">Uma nova lista de reprodução foi atribuída a **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="7f69e-139">A new playlist has been assigned to **currentPlaylist**.</span></span>                                                                                               |
| <span data-ttu-id="7f69e-140">8</span><span class="sxs-lookup"><span data-stu-id="7f69e-140">8</span></span>     | <span data-ttu-id="7f69e-141">MediaChanging</span><span class="sxs-lookup"><span data-stu-id="7f69e-141">MediaChanging</span></span>           | <span data-ttu-id="7f69e-142">Um novo item de mídia está prestes a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="7f69e-142">A new media item is about to be loaded.</span></span>                                                                                                                |
| <span data-ttu-id="7f69e-143">9</span><span class="sxs-lookup"><span data-stu-id="7f69e-143">9</span></span>     | <span data-ttu-id="7f69e-144">MediaLocating</span><span class="sxs-lookup"><span data-stu-id="7f69e-144">MediaLocating</span></span>           | <span data-ttu-id="7f69e-145">O Windows Media Player está localizando o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="7f69e-145">Windows Media Player is locating the media item.</span></span> <span data-ttu-id="7f69e-146">O arquivo pode ser local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-146">The file can be local or remote.</span></span>                                                                      |
| <span data-ttu-id="7f69e-147">10</span><span class="sxs-lookup"><span data-stu-id="7f69e-147">10</span></span>    | <span data-ttu-id="7f69e-148">MediaConnecting</span><span class="sxs-lookup"><span data-stu-id="7f69e-148">MediaConnecting</span></span>         | <span data-ttu-id="7f69e-149">Conectando-se ao servidor que contém o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="7f69e-149">Connecting to the server that holds the media item.</span></span>                                                                                                    |
| <span data-ttu-id="7f69e-150">11</span><span class="sxs-lookup"><span data-stu-id="7f69e-150">11</span></span>    | <span data-ttu-id="7f69e-151">MediaLoading</span><span class="sxs-lookup"><span data-stu-id="7f69e-151">MediaLoading</span></span>            | <span data-ttu-id="7f69e-152">O item de mídia está localizado e agora está sendo recuperado.</span><span class="sxs-lookup"><span data-stu-id="7f69e-152">Media item has been located and is now being retrieved.</span></span>                                                                                                |
| <span data-ttu-id="7f69e-153">12</span><span class="sxs-lookup"><span data-stu-id="7f69e-153">12</span></span>    | <span data-ttu-id="7f69e-154">MediaOpening</span><span class="sxs-lookup"><span data-stu-id="7f69e-154">MediaOpening</span></span>            | <span data-ttu-id="7f69e-155">O item de mídia foi recuperado e agora está sendo aberto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-155">Media item has been retrieved and is now being opened.</span></span>                                                                                                 |
| <span data-ttu-id="7f69e-156">13</span><span class="sxs-lookup"><span data-stu-id="7f69e-156">13</span></span>    | <span data-ttu-id="7f69e-157">MediaOpen</span><span class="sxs-lookup"><span data-stu-id="7f69e-157">MediaOpen</span></span>               | <span data-ttu-id="7f69e-158">O item de mídia está aberto agora.</span><span class="sxs-lookup"><span data-stu-id="7f69e-158">Media item is now open.</span></span>                                                                                                                                |
| <span data-ttu-id="7f69e-159">14</span><span class="sxs-lookup"><span data-stu-id="7f69e-159">14</span></span>    | <span data-ttu-id="7f69e-160">BeginCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="7f69e-160">BeginCodecAcquisition</span></span>   | <span data-ttu-id="7f69e-161">Iniciando a aquisição do codec.</span><span class="sxs-lookup"><span data-stu-id="7f69e-161">Starting codec acquisition.</span></span>                                                                                                                            |
| <span data-ttu-id="7f69e-162">15</span><span class="sxs-lookup"><span data-stu-id="7f69e-162">15</span></span>    | <span data-ttu-id="7f69e-163">EndCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="7f69e-163">EndCodecAcquisition</span></span>     | <span data-ttu-id="7f69e-164">A aquisição do codec foi concluída.</span><span class="sxs-lookup"><span data-stu-id="7f69e-164">Codec acquisition is complete.</span></span>                                                                                                                         |
| <span data-ttu-id="7f69e-165">16</span><span class="sxs-lookup"><span data-stu-id="7f69e-165">16</span></span>    | <span data-ttu-id="7f69e-166">BeginLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="7f69e-166">BeginLicenseAcquisition</span></span> | <span data-ttu-id="7f69e-167">Aquisição de uma licença para reproduzir conteúdo protegido por DRM.</span><span class="sxs-lookup"><span data-stu-id="7f69e-167">Acquiring a license to play DRM protected content.</span></span>                                                                                                     |
| <span data-ttu-id="7f69e-168">17</span><span class="sxs-lookup"><span data-stu-id="7f69e-168">17</span></span>    | <span data-ttu-id="7f69e-169">EndLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="7f69e-169">EndLicenseAcquisition</span></span>   | <span data-ttu-id="7f69e-170">A licença para reproduzir conteúdo protegido por DRM foi adquirida.</span><span class="sxs-lookup"><span data-stu-id="7f69e-170">License to play DRM protected content has been acquired.</span></span>                                                                                               |
| <span data-ttu-id="7f69e-171">18</span><span class="sxs-lookup"><span data-stu-id="7f69e-171">18</span></span>    | <span data-ttu-id="7f69e-172">BeginIndividualization</span><span class="sxs-lookup"><span data-stu-id="7f69e-172">BeginIndividualization</span></span>  | <span data-ttu-id="7f69e-173">Inicie a individualização DRM.</span><span class="sxs-lookup"><span data-stu-id="7f69e-173">Begin DRM Individualization.</span></span>                                                                                                                           |
| <span data-ttu-id="7f69e-174">19</span><span class="sxs-lookup"><span data-stu-id="7f69e-174">19</span></span>    | <span data-ttu-id="7f69e-175">Endindividualização</span><span class="sxs-lookup"><span data-stu-id="7f69e-175">EndIndividualization</span></span>    | <span data-ttu-id="7f69e-176">A individualização de DRM foi concluída.</span><span class="sxs-lookup"><span data-stu-id="7f69e-176">DRM individualization has been completed.</span></span>                                                                                                              |
| <span data-ttu-id="7f69e-177">20</span><span class="sxs-lookup"><span data-stu-id="7f69e-177">20</span></span>    | <span data-ttu-id="7f69e-178">MediaWaiting</span><span class="sxs-lookup"><span data-stu-id="7f69e-178">MediaWaiting</span></span>            | <span data-ttu-id="7f69e-179">Aguardando item de mídia.</span><span class="sxs-lookup"><span data-stu-id="7f69e-179">Waiting for media item.</span></span>                                                                                                                                |
| <span data-ttu-id="7f69e-180">21</span><span class="sxs-lookup"><span data-stu-id="7f69e-180">21</span></span>    | <span data-ttu-id="7f69e-181">OpeningUnknownURL</span><span class="sxs-lookup"><span data-stu-id="7f69e-181">OpeningUnknownURL</span></span>       | <span data-ttu-id="7f69e-182">Abrindo uma URL com um tipo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7f69e-182">Opening a URL with an unknown type.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="7f69e-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f69e-183">Remarks</span></span>

<span data-ttu-id="7f69e-184">Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="7f69e-184">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="7f69e-185">Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="7f69e-185">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="7f69e-186">Você não deve escrever código que dependa da ordem de estado.</span><span class="sxs-lookup"><span data-stu-id="7f69e-186">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f69e-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f69e-187">Requirements</span></span>



| <span data-ttu-id="7f69e-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f69e-188">Requirement</span></span> | <span data-ttu-id="7f69e-189">Valor</span><span class="sxs-lookup"><span data-stu-id="7f69e-189">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f69e-190">Versão</span><span class="sxs-lookup"><span data-stu-id="7f69e-190">Version</span></span><br/> | <span data-ttu-id="7f69e-191">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7f69e-191">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7f69e-192">DLL</span><span class="sxs-lookup"><span data-stu-id="7f69e-192">DLL</span></span><br/>     | <dl> <span data-ttu-id="7f69e-193"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f69e-193"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f69e-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f69e-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f69e-195">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="7f69e-195">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="7f69e-196">**Evento Player. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="7f69e-196">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 





