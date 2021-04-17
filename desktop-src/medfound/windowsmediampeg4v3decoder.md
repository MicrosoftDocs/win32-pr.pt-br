---
description: O decodificador do Windows Media MPEG-4 v3 decodifica fluxos de vídeo MPEG-4 v3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Decodificador do Windows Media MPEG-4 v3 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105768356"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a><span data-ttu-id="7f545-103">Decodificador do Windows Media MPEG-4 v3</span><span class="sxs-lookup"><span data-stu-id="7f545-103">Windows Media MPEG-4 V3 Decoder</span></span>

<span data-ttu-id="7f545-104">O decodificador do Windows Media MPEG-4 v3 decodifica fluxos de vídeo MPEG-4 v3.</span><span class="sxs-lookup"><span data-stu-id="7f545-104">The Windows Media MPEG-4 V3 decoder decodes MPEG-4 V3 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="7f545-105">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="7f545-105">Class Identifier</span></span>

<span data-ttu-id="7f545-106">O CLSID (identificador de classe) para o decodificador do Windows MPEG-4 v3 é representado pela constante **CLSID \_ CMpeg43DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="7f545-106">The class identifier (CLSID) for the Windows MPEG-4 V3 decoder is represented by the constant **CLSID\_CMpeg43DecMediaObject**.</span></span> <span data-ttu-id="7f545-107">Você pode criar uma instância do decodificador MPEG-4 v3 chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="7f545-107">You can create an instance of the MPEG-4 V3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="7f545-108">Formatos</span><span class="sxs-lookup"><span data-stu-id="7f545-108">Formats</span></span>

<span data-ttu-id="7f545-109">O decodificador do Windows Media MPEG-4 v3 dá suporte aos seguintes tipos de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="7f545-109">The Windows Media MPEG-4 V3 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="7f545-110">MEDIASUBTYPE \_ MP43</span><span class="sxs-lookup"><span data-stu-id="7f545-110">MEDIASUBTYPE\_MP43</span></span>
-   <span data-ttu-id="7f545-111">MEDIASUBTYPE \_ mp43</span><span class="sxs-lookup"><span data-stu-id="7f545-111">MEDIASUBTYPE\_mp43</span></span>

<span data-ttu-id="7f545-112">O decodificador do Windows Media MPEG-4 v3 dá suporte aos seguintes subtipos de mídia de saída quando ele está agindo como um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="7f545-112">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="7f545-113">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="7f545-113">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="7f545-114">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="7f545-114">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="7f545-115">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="7f545-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="7f545-116">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="7f545-116">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="7f545-117">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="7f545-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="7f545-118">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="7f545-118">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="7f545-119">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="7f545-119">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="7f545-120">O decodificador do Windows Media MPEG-4 v3 dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="7f545-120">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="7f545-121">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="7f545-121">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="7f545-122">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="7f545-122">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="7f545-123">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="7f545-123">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="7f545-124">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="7f545-124">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="7f545-125">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="7f545-125">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="7f545-126">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="7f545-126">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="7f545-127">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="7f545-127">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="7f545-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f545-128">Remarks</span></span>

<span data-ttu-id="7f545-129">O objeto decodificador do Windows Media MPEG-4 v3 expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="7f545-129">The Windows Media MPEG-4 V3 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="7f545-130">O objeto tem o mesmo identificador de classe (CLSID), independentemente de atuar como um DMO ou MFT.</span><span class="sxs-lookup"><span data-stu-id="7f545-130">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="7f545-131">O decodificador MPEG-4 v3 se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está em execução.</span><span class="sxs-lookup"><span data-stu-id="7f545-131">The MPEG-4 V3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="7f545-132">A tabela a seguir mostra as condições sob as quais um decodificador MPEG-4 v3 se comporta como um DMO ou uma MFT.</span><span class="sxs-lookup"><span data-stu-id="7f545-132">The following table shows the conditions under which an MPEG-4 V3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="7f545-133">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="7f545-133">Operating system</span></span>            | <span data-ttu-id="7f545-134">Comportamento do decodificador</span><span class="sxs-lookup"><span data-stu-id="7f545-134">Decoder behavior</span></span>                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f545-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f545-135">Windows XP</span></span>                  | <span data-ttu-id="7f545-136">O decodificador MPEG-4 v3 sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="7f545-136">The MPEG-4 V3 decoder always behaves as a DMO.</span></span>                                                                                                                      |
| <span data-ttu-id="7f545-137">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f545-137">Windows Vista and Windows 7</span></span> | <span data-ttu-id="7f545-138">Por padrão, o decodificador MPEG-4 v3 se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="7f545-138">By default, the MPEG-4 V3 decoder behaves as a DMO.</span></span> <span data-ttu-id="7f545-139">Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) no decodificador MPEG-4 v3, ele se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="7f545-139">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on the MPEG-4 V3 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="7f545-140">Os identificadores globalmente exclusivos (GUIDs) para subtipos de mídia RGB diferem dependendo se um decodificador está agindo como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="7f545-140">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="7f545-141">Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um decodificador estar agindo como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="7f545-141">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="7f545-142">Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7f545-142">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f545-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f545-143">Requirements</span></span>



| <span data-ttu-id="7f545-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f545-144">Requirement</span></span> | <span data-ttu-id="7f545-145">Valor</span><span class="sxs-lookup"><span data-stu-id="7f545-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f545-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f545-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7f545-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f545-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7f545-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f545-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7f545-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f545-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f545-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f545-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f545-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f545-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="7f545-152">DLL</span><span class="sxs-lookup"><span data-stu-id="7f545-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f545-153"><dt>MP43DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f545-153"><dt>MP43DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f545-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f545-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f545-155">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="7f545-155">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
