---
description: Objetos de streaming multimídia
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Objetos de streaming multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297986"
---
# <a name="multimedia-streaming-objects"></a><span data-ttu-id="fd49a-103">Objetos de streaming multimídia</span><span class="sxs-lookup"><span data-stu-id="fd49a-103">Multimedia Streaming Objects</span></span>

> [!Note]  
> <span data-ttu-id="fd49a-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="fd49a-104">This API is deprecated.</span></span> <span data-ttu-id="fd49a-105">Novos aplicativos não devem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="fd49a-105">New applications should not use it.</span></span>

 

<span data-ttu-id="fd49a-106">A tabela a seguir descreve os objetos de streaming de multimídia.</span><span class="sxs-lookup"><span data-stu-id="fd49a-106">The following table describes the multimedia streaming objects.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd49a-107">CLSID</span><span class="sxs-lookup"><span data-stu-id="fd49a-107">CLSID</span></span></th>
<th><span data-ttu-id="fd49a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd49a-108">Description</span></span></th>
<th><span data-ttu-id="fd49a-109">Interfaces com suporte</span><span class="sxs-lookup"><span data-stu-id="fd49a-109">Interfaces supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd49a-110">CLSID_AMMediaTypeStream</span><span class="sxs-lookup"><span data-stu-id="fd49a-110">CLSID_AMMediaTypeStream</span></span></td>
<td><span data-ttu-id="fd49a-111">Pode criar amostras de mídia para qualquer tipo de dados com suporte do DirectShow</span><span class="sxs-lookup"><span data-stu-id="fd49a-111">Can create media samples for any DirectShow-supported data type</span></span></td>
<td><ul>
<li><span data-ttu-id="fd49a-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd49a-116">CLSID_AMAudioData</span><span class="sxs-lookup"><span data-stu-id="fd49a-116">CLSID_AMAudioData</span></span></td>
<td><span data-ttu-id="fd49a-117">Implementação do objeto de contêiner <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> Audio.</span><span class="sxs-lookup"><span data-stu-id="fd49a-117">Implementation of <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> audio container object.</span></span></td>
<td><ul>
<li><span data-ttu-id="fd49a-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd49a-119">CLSID_AMDirectDrawStream</span><span class="sxs-lookup"><span data-stu-id="fd49a-119">CLSID_AMDirectDrawStream</span></span></td>
<td><span data-ttu-id="fd49a-120">O fluxo de mídia do DirectDraw que pode ser adicionado a um fluxo multimídia do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fd49a-120">DirectDraw media stream that can be added to a DirectShow multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="fd49a-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd49a-126">CLSID_AMMultiMediaStream</span><span class="sxs-lookup"><span data-stu-id="fd49a-126">CLSID_AMMultiMediaStream</span></span></td>
<td><span data-ttu-id="fd49a-127">Implementação do DirectShow do fluxo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="fd49a-127">DirectShow implementation of multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="fd49a-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd49a-130">CLSID_MediaStreamFilter</span><span class="sxs-lookup"><span data-stu-id="fd49a-130">CLSID_MediaStreamFilter</span></span></td>
<td><span data-ttu-id="fd49a-131">Fornece a funcionalidade de streaming de multimídia para o objeto CLSID_AMMultiMediaStream por meio da interface <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fd49a-131">Provides multimedia streaming functionality for the CLSID_AMMultiMediaStream object through the <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> interface.</span></span></td>
<td><ul>
<li><span data-ttu-id="fd49a-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd49a-133">N/D</span><span class="sxs-lookup"><span data-stu-id="fd49a-133">N/A</span></span></td>
<td><span data-ttu-id="fd49a-134">Exemplos criados pelo objeto CLSID_AMMediaTypeStream.</span><span class="sxs-lookup"><span data-stu-id="fd49a-134">Samples created by the CLSID_AMMediaTypeStream object.</span></span></td>
<td><ul>
<li><span data-ttu-id="fd49a-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd49a-138">N/D</span><span class="sxs-lookup"><span data-stu-id="fd49a-138">N/A</span></span></td>
<td><span data-ttu-id="fd49a-139">Exemplos criados pelo fluxo do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="fd49a-139">Samples created by the DirectDraw stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="fd49a-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="fd49a-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd49a-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



