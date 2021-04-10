---
title: Interface do IMsRdpCameraRedirConfigCollection
description: Representa a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota da interface IMsRdpCameraRedirConfigCollection, descrita
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104087193"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a><span data-ttu-id="b805b-105">Interface do IMsRdpCameraRedirConfigCollection</span><span class="sxs-lookup"><span data-stu-id="b805b-105">IMsRdpCameraRedirConfigCollection interface</span></span>

 <span data-ttu-id="b805b-106">Representa a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="b805b-106">Represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="b805b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b805b-107">Members</span></span>

<span data-ttu-id="b805b-108">A interface **IMsRdpCameraRedirConfigCollection** herda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="b805b-108">The **IMsRdpCameraRedirConfigCollection** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="b805b-109">**IMsRdpCameraRedirConfigCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b805b-109">**IMsRdpCameraRedirConfigCollection** also has these types of members:</span></span>

- [<span data-ttu-id="b805b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b805b-110">Methods</span></span>](#methods)
- [<span data-ttu-id="b805b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b805b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b805b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b805b-112">Methods</span></span>

<span data-ttu-id="b805b-113">A interface **IMsRdpCameraRedirConfigCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b805b-113">The **IMsRdpCameraRedirConfigCollection** interface has these methods.</span></span>

| <span data-ttu-id="b805b-114">Método</span><span class="sxs-lookup"><span data-stu-id="b805b-114">Method</span></span>            | <span data-ttu-id="b805b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b805b-115">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="b805b-116">**Addconfig**</span><span class="sxs-lookup"><span data-stu-id="b805b-116">**AddConfig**</span></span>](imsrdpcameraredirconfigcollection-addconfig.md)       |  <span data-ttu-id="b805b-117">Adiciona um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à coleção (a câmera correspondente não precisa estar conectada).</span><span class="sxs-lookup"><span data-stu-id="b805b-117">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>                   |
| [<span data-ttu-id="b805b-118">**Examinar novamente**</span><span class="sxs-lookup"><span data-stu-id="b805b-118">**Rescan**</span></span>](imsrdpcameraredirconfigcollection-rescan.md)       |  <span data-ttu-id="b805b-119">Enumera os dispositivos de câmera conectados.</span><span class="sxs-lookup"><span data-stu-id="b805b-119">Enumerates connected camera devices.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="b805b-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b805b-120">Properties</span></span>

<span data-ttu-id="b805b-121">A interface **IMsRdpCameraRedirConfigCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b805b-121">The **IMsRdpCameraRedirConfigCollection** interface has these properties.</span></span>

| <span data-ttu-id="b805b-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b805b-122">Property</span></span>         | <span data-ttu-id="b805b-123">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b805b-123">Access type</span></span>           | <span data-ttu-id="b805b-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="b805b-124">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="b805b-125">**ByIndex**</span><span class="sxs-lookup"><span data-stu-id="b805b-125">**ByIndex**</span></span>](imsrdpcameraredirconfigcollection-byindex.md)      | <span data-ttu-id="b805b-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b805b-126">Read-only</span></span> |  <span data-ttu-id="b805b-127">Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por seu índice na coleção.</span><span class="sxs-lookup"><span data-stu-id="b805b-127">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>   |
| [<span data-ttu-id="b805b-128">**ByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="b805b-128">**ByInstanceId**</span></span>](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | <span data-ttu-id="b805b-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b805b-129">Read-only</span></span> |    <span data-ttu-id="b805b-130">Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde à ID de instância especificada.</span><span class="sxs-lookup"><span data-stu-id="b805b-130">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>    |
| [<span data-ttu-id="b805b-131">**BySymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="b805b-131">**BySymbolicLink**</span></span>](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | <span data-ttu-id="b805b-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b805b-132">Read-only</span></span> |  <span data-ttu-id="b805b-133">Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde ao link simbólico fornecido da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.</span><span class="sxs-lookup"><span data-stu-id="b805b-133">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>  |
| [<span data-ttu-id="b805b-134">**Contar**</span><span class="sxs-lookup"><span data-stu-id="b805b-134">**Count**</span></span>](imsrdpcameraredirconfigcollection-count.md)                       | <span data-ttu-id="b805b-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b805b-135">Read-only</span></span> |    <span data-ttu-id="b805b-136">Retorna o número de objetos [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="b805b-136">Returns the number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>   |
| [<span data-ttu-id="b805b-137">**EncodeVideo**</span><span class="sxs-lookup"><span data-stu-id="b805b-137">**EncodeVideo**</span></span>](imsrdpcameraredirconfigcollection-encodevideo.md)      | <span data-ttu-id="b805b-138">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="b805b-138">Read/Write</span></span> |  <span data-ttu-id="b805b-139">Especifica se o fluxo de vídeo é ou não codificado em H. 264.</span><span class="sxs-lookup"><span data-stu-id="b805b-139">Specifies whether or not the video stream is H.264 encoded.</span></span>  |
| [<span data-ttu-id="b805b-140">**EncodingQuality**</span><span class="sxs-lookup"><span data-stu-id="b805b-140">**EncodingQuality**</span></span>](imsrdpcameraredirconfigcollection-encodingquality.md)                       | <span data-ttu-id="b805b-141">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="b805b-141">Read/Write</span></span> |    <span data-ttu-id="b805b-142">Especifica a qualidade de codificação (taxa de bits).</span><span class="sxs-lookup"><span data-stu-id="b805b-142">Specifies the encoding quality (bit rate).</span></span>   |
| [<span data-ttu-id="b805b-143">**RedirectByDefault**</span><span class="sxs-lookup"><span data-stu-id="b805b-143">**RedirectByDefault**</span></span>](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | <span data-ttu-id="b805b-144">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="b805b-144">Read/Write</span></span> |   <span data-ttu-id="b805b-145">Especifica se uma nova câmera será redirecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="b805b-145">Specifies whether or not any new camera gets redirected by default.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="b805b-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b805b-146">Requirements</span></span>

| <span data-ttu-id="b805b-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b805b-147">Requirement</span></span> | <span data-ttu-id="b805b-148">Valor</span><span class="sxs-lookup"><span data-stu-id="b805b-148">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="b805b-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b805b-149">Minimum supported client</span></span>| <span data-ttu-id="b805b-150">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="b805b-150">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="b805b-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b805b-151">Type library</span></span>            | <span data-ttu-id="b805b-152">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b805b-152">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="b805b-153">DLL</span><span class="sxs-lookup"><span data-stu-id="b805b-153">DLL</span></span>                  | <span data-ttu-id="b805b-154">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b805b-154">MsTscAx.dll</span></span>     |
| <span data-ttu-id="b805b-155">IID</span><span class="sxs-lookup"><span data-stu-id="b805b-155">IID</span></span>                      | <span data-ttu-id="b805b-156">IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="b805b-156">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>            |

## <a name="see-also"></a><span data-ttu-id="b805b-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="b805b-157">See also</span></span>

- [<span data-ttu-id="b805b-158">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="b805b-158">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
- [<span data-ttu-id="b805b-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="b805b-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
