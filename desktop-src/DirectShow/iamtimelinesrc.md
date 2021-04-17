---
description: A interface IAMTimelineSrc fornece métodos para manipular e definir propriedades em objetos de origem nos serviços de edição do DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interface IAMTimelineSrc (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812827"
---
# <a name="iamtimelinesrc-interface"></a><span data-ttu-id="f0482-103">Interface IAMTimelineSrc</span><span class="sxs-lookup"><span data-stu-id="f0482-103">IAMTimelineSrc interface</span></span>

> [!Note]  
> <span data-ttu-id="f0482-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f0482-104">\[Deprecated.</span></span> <span data-ttu-id="f0482-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f0482-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f0482-106">A `IAMTimelineSrc` interface fornece métodos para manipular e definir propriedades em objetos de origem nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="f0482-106">The `IAMTimelineSrc` interface provides methods for manipulating and setting properties on source objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="f0482-107">Um objeto de origem representa um fluxo de uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="f0482-107">A source object represents one stream from a media source.</span></span>

<span data-ttu-id="f0482-108">Você pode usar uma parte dos dados em um arquivo de origem definindo as horas de início e de parada de mídia.</span><span class="sxs-lookup"><span data-stu-id="f0482-108">You can use a portion of the data within a source file by setting the media start and media stop times.</span></span> <span data-ttu-id="f0482-109">Esses valores especificam o início e o fim do objeto de origem, em relação à origem da mídia original.</span><span class="sxs-lookup"><span data-stu-id="f0482-109">These values specify the beginning and end of the source object, relative to the original media source.</span></span> <span data-ttu-id="f0482-110">As horas de mídia podem diferir das horas de início e parada do objeto na linha do tempo, permitindo a reprodução de movimento rápido ou lento.</span><span class="sxs-lookup"><span data-stu-id="f0482-110">The media times can differ from the object's start and stop times on the timeline, allowing for fast- or slow-motion playback.</span></span> <span data-ttu-id="f0482-111">(Com fontes de áudio, ocorre a mudança de densidade.)</span><span class="sxs-lookup"><span data-stu-id="f0482-111">(With audio sources, pitch shifting occurs.)</span></span>

<span data-ttu-id="f0482-112">Para criar um objeto de origem, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha de tempo \_ principal \_ tipo \_ Source.</span><span class="sxs-lookup"><span data-stu-id="f0482-112">To create a source object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_SOURCE.</span></span> <span data-ttu-id="f0482-113">Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a interface **IAMTimelineSrc** .</span><span class="sxs-lookup"><span data-stu-id="f0482-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineSrc** interface.</span></span> <span data-ttu-id="f0482-114">Para obter mais informações, consulte [construindo uma linha do tempo](constructing-a-timeline.md) e [trabalhando com fontes](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="f0482-114">For more information, see [Constructing a Timeline](constructing-a-timeline.md) and [Working with Sources](working-with-sources.md).</span></span>

## <a name="members"></a><span data-ttu-id="f0482-115">Membros</span><span class="sxs-lookup"><span data-stu-id="f0482-115">Members</span></span>

<span data-ttu-id="f0482-116">A interface **IAMTimelineSrc** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f0482-116">The **IAMTimelineSrc** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f0482-117">**IAMTimelineSrc** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f0482-117">**IAMTimelineSrc** also has these types of members:</span></span>

-   [<span data-ttu-id="f0482-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="f0482-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f0482-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="f0482-119">Methods</span></span>

<span data-ttu-id="f0482-120">A interface **IAMTimelineSrc** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f0482-120">The **IAMTimelineSrc** interface has these methods.</span></span>



| <span data-ttu-id="f0482-121">Método</span><span class="sxs-lookup"><span data-stu-id="f0482-121">Method</span></span>                                                    | <span data-ttu-id="f0482-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0482-122">Description</span></span>                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0482-123">**FixMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="f0482-123">**FixMediaTimes**</span></span>](iamtimelinesrc-fixmediatimes.md)     | <span data-ttu-id="f0482-124">Arredonda os valores de tempo especificados para o limite de quadro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="f0482-124">Rounds the specified time values to the nearest frame boundary.</span></span><br/>                               |
| [<span data-ttu-id="f0482-125">**FixMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="f0482-125">**FixMediaTimes2**</span></span>](iamtimelinesrc-fixmediatimes2.md)   | <span data-ttu-id="f0482-126">Arredonda os valores de tempo especificados, fornecidos como valores de **REFTIME** , para o limite de quadro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="f0482-126">Rounds the specified time values, given as **REFTIME** values, to the nearest frame boundary.</span></span><br/> |
| [<span data-ttu-id="f0482-127">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="f0482-127">**GetDefaultFPS**</span></span>](iamtimelinesrc-getdefaultfps.md)     | <span data-ttu-id="f0482-128">Recupera a taxa de quadros padrão do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-128">Retrieves the source object's default frame rate.</span></span><br/>                                             |
| [<span data-ttu-id="f0482-129">**GetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="f0482-129">**GetMediaLength**</span></span>](iamtimelinesrc-getmedialength.md)   | <span data-ttu-id="f0482-130">Recupera o tamanho da mídia deste objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-130">Retrieves the media length of this source object.</span></span><br/>                                             |
| [<span data-ttu-id="f0482-131">**GetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="f0482-131">**GetMediaLength2**</span></span>](iamtimelinesrc-getmedialength2.md) | <span data-ttu-id="f0482-132">Recupera o tamanho da mídia desse objeto de origem, como um valor de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="f0482-132">Retrieves the media length of this source object, as a **REFTIME** value.</span></span><br/>                     |
| [<span data-ttu-id="f0482-133">**Getmedianame**</span><span class="sxs-lookup"><span data-stu-id="f0482-133">**GetMediaName**</span></span>](iamtimelinesrc-getmedianame.md)       | <span data-ttu-id="f0482-134">Recupera o nome do arquivo de origem representado por esse objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-134">Retrieves the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="f0482-135">**GetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="f0482-135">**GetMediaTimes**</span></span>](iamtimelinesrc-getmediatimes.md)     | <span data-ttu-id="f0482-136">Recupera os horários de início e de término da mídia.</span><span class="sxs-lookup"><span data-stu-id="f0482-136">Retrieves the media start and stop times.</span></span><br/>                                                     |
| [<span data-ttu-id="f0482-137">**GetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="f0482-137">**GetMediaTimes2**</span></span>](iamtimelinesrc-getmediatimes2.md)   | <span data-ttu-id="f0482-138">Recupera os horários de início e de parada da mídia, como valores de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="f0482-138">Retrieves the media start and stop times, as **REFTIME** values.</span></span><br/>                              |
| [<span data-ttu-id="f0482-139">**GetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="f0482-139">**GetStreamNumber**</span></span>](iamtimelinesrc-getstreamnumber.md) | <span data-ttu-id="f0482-140">Recupera o número de fluxo atual para o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-140">Retrieves the current stream number for the source object.</span></span><br/>                                    |
| [<span data-ttu-id="f0482-141">**Getalongamode**</span><span class="sxs-lookup"><span data-stu-id="f0482-141">**GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)   | <span data-ttu-id="f0482-142">Recupera o modo de ampliação de uma fonte de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f0482-142">Retrieves the stretch mode of a video source.</span></span><br/>                                                 |
| [<span data-ttu-id="f0482-143">**IsNormalRate**</span><span class="sxs-lookup"><span data-stu-id="f0482-143">**IsNormalRate**</span></span>](iamtimelinesrc-isnormalrate.md)       | <span data-ttu-id="f0482-144">Indica se o clipe será reproduzido na taxa de reprodução normal.</span><span class="sxs-lookup"><span data-stu-id="f0482-144">Indicates whether the clip will play at the normal playback rate.</span></span><br/>                             |
| [<span data-ttu-id="f0482-145">**ModifyStopTime**</span><span class="sxs-lookup"><span data-stu-id="f0482-145">**ModifyStopTime**</span></span>](iamtimelinesrc-modifystoptime.md)   | <span data-ttu-id="f0482-146">Define a hora de parada, em relação à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="f0482-146">Sets the stop time, relative to the timeline.</span></span><br/>                                                 |
| [<span data-ttu-id="f0482-147">**ModifyStopTime2**</span><span class="sxs-lookup"><span data-stu-id="f0482-147">**ModifyStopTime2**</span></span>](iamtimelinesrc-modifystoptime2.md) | <span data-ttu-id="f0482-148">Define a hora de parada, como um valor de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="f0482-148">Sets the stop time, as a **REFTIME** value.</span></span><br/>                                                   |
| [<span data-ttu-id="f0482-149">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="f0482-149">**SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)     | <span data-ttu-id="f0482-150">Define a taxa de quadros padrão do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-150">Sets the source object's default frame rate.</span></span><br/>                                                  |
| [<span data-ttu-id="f0482-151">**SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="f0482-151">**SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)   | <span data-ttu-id="f0482-152">Especifica a duração do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-152">Specifies the duration of the source file.</span></span><br/>                                                    |
| [<span data-ttu-id="f0482-153">**SetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="f0482-153">**SetMediaLength2**</span></span>](iamtimelinesrc-setmedialength2.md) | <span data-ttu-id="f0482-154">Especifica a duração do arquivo de origem, como um valor **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="f0482-154">Specifies the duration of the source file, as a **REFTIME** value.</span></span><br/>                            |
| [<span data-ttu-id="f0482-155">**Setmedianame**</span><span class="sxs-lookup"><span data-stu-id="f0482-155">**SetMediaName**</span></span>](iamtimelinesrc-setmedianame.md)       | <span data-ttu-id="f0482-156">Especifica o nome do arquivo de origem representado por esse objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-156">Specifies the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="f0482-157">**SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="f0482-157">**SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)     | <span data-ttu-id="f0482-158">Define as horas de início e de término da mídia.</span><span class="sxs-lookup"><span data-stu-id="f0482-158">Sets the media stop and start times.</span></span><br/>                                                          |
| [<span data-ttu-id="f0482-159">**SetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="f0482-159">**SetMediaTimes2**</span></span>](iamtimelinesrc-setmediatimes2.md)   | <span data-ttu-id="f0482-160">Define as horas de parada e de início da mídia, como valores de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="f0482-160">Sets the media stop and start times, as **REFTIME** values.</span></span><br/>                                   |
| [<span data-ttu-id="f0482-161">**SetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="f0482-161">**SetStreamNumber**</span></span>](iamtimelinesrc-setstreamnumber.md) | <span data-ttu-id="f0482-162">Especifica qual fluxo deve ser lido do arquivo de origem associado a este objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-162">Specifies which stream to read from the source file associated with this source object.</span></span><br/>       |
| [<span data-ttu-id="f0482-163">**Setstretchmode**</span><span class="sxs-lookup"><span data-stu-id="f0482-163">**SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)   | <span data-ttu-id="f0482-164">Define o modo de ampliação de uma fonte de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f0482-164">Sets the stretch mode of a video source.</span></span><br/>                                                      |
| [<span data-ttu-id="f0482-165">**SpliceWithNext**</span><span class="sxs-lookup"><span data-stu-id="f0482-165">**SpliceWithNext**</span></span>](iamtimelinesrc-splicewithnext.md)   | <span data-ttu-id="f0482-166">Une esse objeto de origem a outro objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0482-166">Joins this source object to another source object.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="f0482-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0482-167">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0482-168">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f0482-168">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0482-169">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0482-169">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f0482-170">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f0482-170">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0482-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0482-171">Requirements</span></span>



| <span data-ttu-id="f0482-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0482-172">Requirement</span></span> | <span data-ttu-id="f0482-173">Valor</span><span class="sxs-lookup"><span data-stu-id="f0482-173">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0482-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0482-174">Header</span></span><br/>  | <dl> <span data-ttu-id="f0482-175"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0482-175"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f0482-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0482-176">Library</span></span><br/> | <dl> <span data-ttu-id="f0482-177"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0482-177"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
