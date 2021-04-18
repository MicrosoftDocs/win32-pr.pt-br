---
description: O decodificador de tela do Windows Media Video 9 decodifica os fluxos que foram codificados pelo codificador de tela do Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Decodificador de tela do Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784521"
---
# <a name="windows-media-video-9-screen-decoder"></a><span data-ttu-id="a75b6-103">Decodificador de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a75b6-103">Windows Media Video 9 Screen Decoder</span></span>

<span data-ttu-id="a75b6-104">O decodificador de tela do Windows Media Video 9 decodifica os fluxos que foram codificados pelo [**codificador de tela do Windows Media Video 9**](windowsmediavideo9screenencoder.md).</span><span class="sxs-lookup"><span data-stu-id="a75b6-104">The Windows Media Video 9 Screen decoder decodes streams that were encoded by the [**Windows Media Video 9 Screen Encoder**](windowsmediavideo9screenencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a75b6-105">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="a75b6-105">Class Identifier</span></span>

<span data-ttu-id="a75b6-106">O CLSID (identificador de classe) do decodificador de tela do Windows Media Video 9 é representado pela constante **CLSID \_ CMSSCDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="a75b6-106">The class identifier (CLSID) for the Windows Media Video 9 Screen decoder is represented by the constant **CLSID\_CMSSCDecMediaObject**.</span></span> <span data-ttu-id="a75b6-107">Você pode criar uma instância do decodificador chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a75b6-107">You can create an instance of the decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="a75b6-108">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="a75b6-108">Input Types</span></span>

<span data-ttu-id="a75b6-109">O FOURCC (código de quatro caracteres) para o conteúdo codificado da tela de vídeo do Windows Media versão 9 é "MSS2".</span><span class="sxs-lookup"><span data-stu-id="a75b6-109">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="a75b6-110">Os seguintes tipos de entrada são suportados pelo decodificador de tela da versão 9.</span><span class="sxs-lookup"><span data-stu-id="a75b6-110">The following input types are supported by the Version 9 Screen decoder.</span></span>

-   <span data-ttu-id="a75b6-111">MEDIASUBTYPE \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="a75b6-111">MEDIASUBTYPE\_MSS2</span></span>

## <a name="output-types"></a><span data-ttu-id="a75b6-112">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="a75b6-112">Output Types</span></span>

<span data-ttu-id="a75b6-113">Os tipos de saída a seguir têm suporte no decodificador de tela da versão 9 quando ele está sendo usado como um objeto de mídia do DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="a75b6-113">The following output types are supported by the Version 9 Screen decoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="a75b6-114">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="a75b6-114">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="a75b6-115">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="a75b6-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="a75b6-116">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="a75b6-116">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="a75b6-117">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="a75b6-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="a75b6-118">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="a75b6-118">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="a75b6-119">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="a75b6-119">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="a75b6-120">Os tipos de saída a seguir têm suporte no decodificador de tela da versão 9 quando ele está sendo usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="a75b6-120">The following output types are supported by the Version 9 Screen decoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="a75b6-121">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="a75b6-121">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="a75b6-122">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="a75b6-122">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="a75b6-123">MFVideoFormat \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="a75b6-123">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="a75b6-124">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="a75b6-124">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="a75b6-125">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="a75b6-125">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="a75b6-126">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="a75b6-126">MFVideoFormat\_RGB8</span></span>

## <a name="remarks"></a><span data-ttu-id="a75b6-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a75b6-127">Remarks</span></span>

<span data-ttu-id="a75b6-128">Um objeto decodificador de tela expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="a75b6-128">A screen decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="a75b6-129">Um decodificador de tela se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="a75b6-129">A screen decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="a75b6-130">A tabela a seguir mostra as condições sob as quais um decodificador de tela se comporta como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="a75b6-130">The following table shows the conditions under which a screen decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="a75b6-131">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a75b6-131">Operating system</span></span>            | <span data-ttu-id="a75b6-132">Comportamento do decodificador</span><span class="sxs-lookup"><span data-stu-id="a75b6-132">Decoder behavior</span></span>                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a75b6-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a75b6-133">Windows XP</span></span>                  | <span data-ttu-id="a75b6-134">Um decodificador de tela do Windows Media sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="a75b6-134">A Windows Media Screen decoder always behaves as a DMO.</span></span>                                                                                                                 |
| <span data-ttu-id="a75b6-135">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="a75b6-135">Windows Vista and Windows 7</span></span> | <span data-ttu-id="a75b6-136">Por padrão, um decodificador de tela do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="a75b6-136">By default, a Windows Media Screen decoder behaves as a DMO.</span></span> <span data-ttu-id="a75b6-137">Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um decodificador de tela, ela se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="a75b6-137">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a screen decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="a75b6-138">Você pode usar o mesmo CLSID (CLSID \_ CMSSCDecMediaObject) para criar o decodificador de tela da versão 7 e o decodificador de tela da versão 9.</span><span class="sxs-lookup"><span data-stu-id="a75b6-138">You can use the same CLSID (CLSID\_CMSSCDecMediaObject) to create the Version 7 Screen decoder and the Version 9 Screen decoder.</span></span> <span data-ttu-id="a75b6-139">O FOURCC para o conteúdo codificado da tela de vídeo do Windows Media versão 7 é "MSS1".</span><span class="sxs-lookup"><span data-stu-id="a75b6-139">The FOURCC for Windows Media Video Screen Version 7 encoded content is "MSS1".</span></span> <span data-ttu-id="a75b6-140">O decodificador de tela da versão 7 dá suporte ao \_ tipo de entrada MEDIASUBTYPE MSS1.</span><span class="sxs-lookup"><span data-stu-id="a75b6-140">The Version 7 Screen decoder supports the MEDIASUBTYPE\_MSS1 input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75b6-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a75b6-141">Requirements</span></span>



| <span data-ttu-id="a75b6-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a75b6-142">Requirement</span></span> | <span data-ttu-id="a75b6-143">Valor</span><span class="sxs-lookup"><span data-stu-id="a75b6-143">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a75b6-144">Cliente</span><span class="sxs-lookup"><span data-stu-id="a75b6-144">Client</span></span><br/> | <span data-ttu-id="a75b6-145">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="a75b6-145">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="a75b6-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a75b6-146">Header</span></span><br/> | <dl> <span data-ttu-id="a75b6-147"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a75b6-147"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a75b6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a75b6-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="a75b6-149"><dt>Wmvsdecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a75b6-149"><dt>Wmvsdecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a75b6-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="a75b6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a75b6-151">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="a75b6-151">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a75b6-152">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="a75b6-152">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="a75b6-153">Usando o codec de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a75b6-153">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="a75b6-154">Codificador de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a75b6-154">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
