---
description: O decodificador do Windows Media MPEG4 V1/V2 decodifica fluxos de vídeo MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Decodificador do Windows Media MPEG4 V1/V2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105798028"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a><span data-ttu-id="ae5a8-103">Decodificador do Windows Media MPEG4 V1/V2</span><span class="sxs-lookup"><span data-stu-id="ae5a8-103">Windows Media MPEG4 V1/V2 Decoder</span></span>

<span data-ttu-id="ae5a8-104">O decodificador do Windows Media MPEG4 V1/V2 decodifica fluxos de vídeo MPEG4 v1/v2.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-104">The Windows Media MPEG4 V1/V2 decoder decodes MPEG4 V1/V2 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="ae5a8-105">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="ae5a8-105">Class Identifier</span></span>

<span data-ttu-id="ae5a8-106">O CLSID (identificador de classe) para o decodificador MPEG4 v1/v2 do Windows Media é representado pela constante **CLSID \_ CMpeg4DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-106">The class identifier (CLSID) for the Windows Media MPEG4 V1/V2 decoder is represented by the constant **CLSID\_CMpeg4DecMediaObject**.</span></span> <span data-ttu-id="ae5a8-107">Você pode criar uma instância do decodificador MPEG4 V1/V2 chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-107">You can create an instance of the MPEG4 V1/V2 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="ae5a8-108">Formatos</span><span class="sxs-lookup"><span data-stu-id="ae5a8-108">Formats</span></span>

<span data-ttu-id="ae5a8-109">O decodificador MPEG4 v1/v2 do Windows Media dá suporte aos seguintes tipos de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-109">The Windows Media MPEG4 V1/V2 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="ae5a8-110">MEDIASUBTYPE \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="ae5a8-110">MEDIASUBTYPE\_MPG4</span></span>
-   <span data-ttu-id="ae5a8-111">MEDIASUBTYPE \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="ae5a8-111">MEDIASUBTYPE\_mpg4</span></span>
-   <span data-ttu-id="ae5a8-112">MEDIASUBTYPE \_ MP42</span><span class="sxs-lookup"><span data-stu-id="ae5a8-112">MEDIASUBTYPE\_MP42</span></span>
-   <span data-ttu-id="ae5a8-113">MEDIASUBTYPE \_ mp42</span><span class="sxs-lookup"><span data-stu-id="ae5a8-113">MEDIASUBTYPE\_mp42</span></span>

<span data-ttu-id="ae5a8-114">O decodificador do Windows Media MPEG4 V1/V2 dá suporte aos seguintes subtipos de mídia de saída quando ele está agindo como um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="ae5a8-114">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="ae5a8-115">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="ae5a8-115">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="ae5a8-116">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="ae5a8-116">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="ae5a8-117">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="ae5a8-117">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="ae5a8-118">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="ae5a8-118">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="ae5a8-119">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="ae5a8-119">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="ae5a8-120">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="ae5a8-120">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="ae5a8-121">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="ae5a8-121">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="ae5a8-122">O decodificador do Windows Media MPEG4 V1/V2 dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="ae5a8-122">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="ae5a8-123">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="ae5a8-123">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="ae5a8-124">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="ae5a8-124">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="ae5a8-125">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="ae5a8-125">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="ae5a8-126">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="ae5a8-126">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="ae5a8-127">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="ae5a8-127">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="ae5a8-128">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="ae5a8-128">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="ae5a8-129">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="ae5a8-129">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="ae5a8-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae5a8-130">Remarks</span></span>

<span data-ttu-id="ae5a8-131">O objeto decodificador do Windows Media MPEG4 V1/V2 expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="ae5a8-131">The Windows Media MPEG4 V1/V2 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="ae5a8-132">O objeto tem o mesmo identificador de classe (CLSID), independentemente de atuar como um DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-132">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="ae5a8-133">Um decodificador MPEG4 V1/V2 se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está em execução.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-133">An MPEG4 V1/V2 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="ae5a8-134">A tabela a seguir mostra as condições sob as quais um decodificador MPEG4 V1/V2 se comporta como DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-134">The following table shows the conditions under which an MPEG4 V1/V2 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="ae5a8-135">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="ae5a8-135">Operating system</span></span>            | <span data-ttu-id="ae5a8-136">Comportamento do decodificador</span><span class="sxs-lookup"><span data-stu-id="ae5a8-136">Decoder behavior</span></span>                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5a8-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ae5a8-137">Windows XP</span></span>                  | <span data-ttu-id="ae5a8-138">Um decodificador MPEG4 V1/V2 sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-138">An MPEG4 V1/V2 decoder always behaves as a DMO.</span></span>                                                                                                                                 |
| <span data-ttu-id="ae5a8-139">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae5a8-139">Windows Vista and Windows 7</span></span> | <span data-ttu-id="ae5a8-140">Por padrão, um decodificador MPEG4 V1/V2 se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-140">By default, an MPEG4 V1/V2 decoder behaves as a DMO.</span></span> <span data-ttu-id="ae5a8-141">Se você obtiver uma interface de [GUIDs de subtipo de vídeo](video-subtype-guids.md) em um decodificador MPEG4 V1/V2, ele se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-141">If you obtain an [Video Subtype GUIDs](video-subtype-guids.md) interface on an MPEG4 V1/V2 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="ae5a8-142">Os identificadores globalmente exclusivos (GUIDs) para subtipos de mídia RGB diferem dependendo se um decodificador está agindo como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-142">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="ae5a8-143">Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um decodificador estar agindo como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="ae5a8-143">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="ae5a8-144">Para obter informações sobre os GUIDs que representam subtipos de vídeo, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ae5a8-144">For information about the GUIDs that represent video subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae5a8-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae5a8-145">Requirements</span></span>



| <span data-ttu-id="ae5a8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae5a8-146">Requirement</span></span> | <span data-ttu-id="ae5a8-147">Valor</span><span class="sxs-lookup"><span data-stu-id="ae5a8-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5a8-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae5a8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ae5a8-149">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ae5a8-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ae5a8-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae5a8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ae5a8-151">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae5a8-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae5a8-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae5a8-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae5a8-153"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a8-153"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="ae5a8-154">DLL</span><span class="sxs-lookup"><span data-stu-id="ae5a8-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae5a8-155"><dt>MPG4DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a8-155"><dt>MPG4DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae5a8-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae5a8-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae5a8-157">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="ae5a8-157">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
