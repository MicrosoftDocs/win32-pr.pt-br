---
description: O codificador de tela do Windows Media Video 9 é otimizado para codificar capturas de tela sequenciais de monitores de computador.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Codificador de tela do Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771266"
---
# <a name="windows-media-video-9-screen-encoder"></a><span data-ttu-id="091b3-103">Codificador de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="091b3-103">Windows Media Video 9 Screen Encoder</span></span>

<span data-ttu-id="091b3-104">O codificador de tela do Windows Media Video 9 é otimizado para codificar capturas de tela sequenciais de monitores de computador.</span><span class="sxs-lookup"><span data-stu-id="091b3-104">The Windows Media Video 9 Screen encoder is optimized for encoding sequential screen shots from computer monitors.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="091b3-105">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="091b3-105">Class Identifier</span></span>

<span data-ttu-id="091b3-106">O CLSID (identificador de classe) do codificador de tela do Windows Media Video 9 é representado pela constante **CLSID \_ CMSSCEncMediaObject2**.</span><span class="sxs-lookup"><span data-stu-id="091b3-106">The class identifier (CLSID) for the Windows Media Video 9 Screen encoder is represented by the constant **CLSID\_CMSSCEncMediaObject2**.</span></span> <span data-ttu-id="091b3-107">Você pode criar uma instância do codificador chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="091b3-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="091b3-108">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="091b3-108">Input Types</span></span>

<span data-ttu-id="091b3-109">Os seguintes tipos de entrada são suportados pelo codificador de tela da versão 9 quando ele está sendo usado como um objeto de mídia do DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="091b3-109">The following input types are supported by the Version 9 Screen encoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="091b3-110">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="091b3-110">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="091b3-111">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="091b3-111">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="091b3-112">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="091b3-112">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="091b3-113">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="091b3-113">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="091b3-114">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="091b3-114">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="091b3-115">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="091b3-115">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="091b3-116">Os seguintes tipos de entrada são suportados pelo codificador de tela da versão 9 quando ele está sendo usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="091b3-116">The following input types are supported by the Version 9 Screen encoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="091b3-117">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="091b3-117">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="091b3-118">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="091b3-118">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="091b3-119">MFVideoFormat \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="091b3-119">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="091b3-120">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="091b3-120">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="091b3-121">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="091b3-121">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="091b3-122">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="091b3-122">MFVideoFormat\_RGB8</span></span>

## <a name="output-types"></a><span data-ttu-id="091b3-123">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="091b3-123">Output Types</span></span>

<span data-ttu-id="091b3-124">O FOURCC (código de quatro caracteres) para o conteúdo codificado da tela de vídeo do Windows Media versão 9 é "MSS2".</span><span class="sxs-lookup"><span data-stu-id="091b3-124">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="091b3-125">Os tipos de saída a seguir têm suporte no codificador de tela da versão 9.</span><span class="sxs-lookup"><span data-stu-id="091b3-125">The following output types are supported by the Version 9 Screen encoder.</span></span>

-   <span data-ttu-id="091b3-126">MEDIASUBTYPE \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="091b3-126">MEDIASUBTYPE\_MSS2</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="091b3-127">Propriedades do codificador</span><span class="sxs-lookup"><span data-stu-id="091b3-127">Encoder Properties</span></span>

<span data-ttu-id="091b3-128">O codificador de tela do Windows Media Video 9 dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="091b3-128">The Windows Media Video 9 Screen encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="091b3-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="091b3-129">Property</span></span></th>
<th><span data-ttu-id="091b3-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="091b3-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="091b3-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="091b3-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span></span></td>
<td><span data-ttu-id="091b3-132">Especifica a sobrecarga, em bytes por pacote, necessária para o contêiner que é usado para armazenar o conteúdo compactado.</span><span class="sxs-lookup"><span data-stu-id="091b3-132">Specifies the overhead, in bytes per packet, required for the container that is used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="091b3-133">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-133">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-134">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-134">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span><span class="sxs-lookup"><span data-stu-id="091b3-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span></span></td>
<td><span data-ttu-id="091b3-136">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa média de bits (especificada por <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span><span class="sxs-lookup"><span data-stu-id="091b3-136">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span></span><br/> <dl> <span data-ttu-id="091b3-137">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-137">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-138">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-138">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span><span class="sxs-lookup"><span data-stu-id="091b3-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span></span></td>
<td><span data-ttu-id="091b3-140">Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span><span class="sxs-lookup"><span data-stu-id="091b3-140">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span></span><br/> <dl> <span data-ttu-id="091b3-141">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-141">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-142">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-142">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span><span class="sxs-lookup"><span data-stu-id="091b3-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span></span></td>
<td><span data-ttu-id="091b3-144">Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="091b3-144">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="091b3-145">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-145">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-146">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="091b3-146">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="091b3-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span></span></td>
<td><span data-ttu-id="091b3-148">Especifica o número de quadros de vídeo codificados pelo codec.</span><span class="sxs-lookup"><span data-stu-id="091b3-148">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="091b3-149">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-149">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-150">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="091b3-150">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="091b3-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span></span></td>
<td><span data-ttu-id="091b3-152">Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.</span><span class="sxs-lookup"><span data-stu-id="091b3-152">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="091b3-153">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-153">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-154">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="091b3-154">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span><span class="sxs-lookup"><span data-stu-id="091b3-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span></span></td>
<td><span data-ttu-id="091b3-156">Essa propriedade é substituída por <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="091b3-156">This property is superseded by <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span><span class="sxs-lookup"><span data-stu-id="091b3-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span></span></td>
<td><span data-ttu-id="091b3-158">Especifica a complexidade do algoritmo do codificador.</span><span class="sxs-lookup"><span data-stu-id="091b3-158">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="091b3-159">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="091b3-160">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-160">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span><span class="sxs-lookup"><span data-stu-id="091b3-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span></span></td>
<td><span data-ttu-id="091b3-162">Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem na saída do codec.</span><span class="sxs-lookup"><span data-stu-id="091b3-162">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="091b3-163">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-163">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-164">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-164">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="091b3-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span></span></td>
<td><span data-ttu-id="091b3-166">Especifica o número de quadros de vídeo removidos durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="091b3-166">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="091b3-167">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-167">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-168">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="091b3-168">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span><span class="sxs-lookup"><span data-stu-id="091b3-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span></span></td>
<td><span data-ttu-id="091b3-170">Especifica o fim de uma passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="091b3-170">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="091b3-171">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-171">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-172">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-172">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span><span class="sxs-lookup"><span data-stu-id="091b3-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span></span></td>
<td><span data-ttu-id="091b3-174">Especifica o FOURCC que identifica o codificador que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="091b3-174">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="091b3-175">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-175">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-176">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span><span class="sxs-lookup"><span data-stu-id="091b3-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span></span></td>
<td><span data-ttu-id="091b3-178">Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.</span><span class="sxs-lookup"><span data-stu-id="091b3-178">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="091b3-179">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-179">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-180">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-180">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span><span class="sxs-lookup"><span data-stu-id="091b3-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span></span></td>
<td><span data-ttu-id="091b3-182">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="091b3-182">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span><span class="sxs-lookup"><span data-stu-id="091b3-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span></span></td>
<td><span data-ttu-id="091b3-184">Especifica o número máximo de passagens aceitas pelo codec.</span><span class="sxs-lookup"><span data-stu-id="091b3-184">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="091b3-185">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-185">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-186">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="091b3-186">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span><span class="sxs-lookup"><span data-stu-id="091b3-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span></span></td>
<td><span data-ttu-id="091b3-188">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-188">Windows XP and later.</span></span> <span data-ttu-id="091b3-189">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-189">Read/write.</span></span><br/> <span data-ttu-id="091b3-190">Especifica o número de passagens que o codec usará para codificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="091b3-190">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="091b3-191">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-191">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-192">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-192">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="091b3-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span></span></td>
<td><span data-ttu-id="091b3-194">Especifica QP.</span><span class="sxs-lookup"><span data-stu-id="091b3-194">Specifies QP.</span></span> <span data-ttu-id="091b3-195">Os valores possíveis são 1,0 a 31,0.</span><span class="sxs-lookup"><span data-stu-id="091b3-195">Possible values are 1.0 through 31.0.</span></span><br/> <dl> <span data-ttu-id="091b3-196">Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-196">Windows Vista and later.</span></span><br />
<span data-ttu-id="091b3-197">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-197">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span><span class="sxs-lookup"><span data-stu-id="091b3-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span></span></td>
<td><span data-ttu-id="091b3-199">Especifica a taxa média de bits, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) de 2 passagens.</span><span class="sxs-lookup"><span data-stu-id="091b3-199">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="091b3-200">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-200">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-201">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span><span class="sxs-lookup"><span data-stu-id="091b3-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span></span></td>
<td><span data-ttu-id="091b3-203">Especifica a taxa de bits de pico, em bits por segundo, usada para codificação de taxa de bits de variável (VBR) restrita de 2 passagens.</span><span class="sxs-lookup"><span data-stu-id="091b3-203">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="091b3-204">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-204">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-205">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-205">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="091b3-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span></span></td>
<td><span data-ttu-id="091b3-207">Especifica o número de quadros de vídeo passados para o codificador durante o processo de codificação.</span><span class="sxs-lookup"><span data-stu-id="091b3-207">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="091b3-208">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-208">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-209">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="091b3-209">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span><span class="sxs-lookup"><span data-stu-id="091b3-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span></span></td>
<td><span data-ttu-id="091b3-211">Especifica se o codec usará a codificação de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="091b3-211">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="091b3-212">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-212">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-213">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-213">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span><span class="sxs-lookup"><span data-stu-id="091b3-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span></span></td>
<td><span data-ttu-id="091b3-215">Especifica o nível de qualidade real para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).</span><span class="sxs-lookup"><span data-stu-id="091b3-215">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="091b3-216">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-216">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-217">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-217">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="091b3-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="091b3-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span></span></td>
<td><span data-ttu-id="091b3-219">A quantidade de conteúdo, em milissegundos, que pode caber no buffer de modelo.</span><span class="sxs-lookup"><span data-stu-id="091b3-219">The amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="091b3-220">Windows XP e posterior,</span><span class="sxs-lookup"><span data-stu-id="091b3-220">Windows XP and later,</span></span><br />
<span data-ttu-id="091b3-221">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="091b3-221">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="091b3-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="091b3-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span></span></td>
<td><span data-ttu-id="091b3-223">Especifica o número de quadros de vídeo que foram ignorados porque eles eram duplicatas de quadros anteriores.</span><span class="sxs-lookup"><span data-stu-id="091b3-223">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="091b3-224">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="091b3-224">Windows XP and later.</span></span><br />
<span data-ttu-id="091b3-225">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="091b3-225">Read-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="091b3-226">Comentários</span><span class="sxs-lookup"><span data-stu-id="091b3-226">Remarks</span></span>

<span data-ttu-id="091b3-227">Um objeto de codificador de tela expõe a interface **IMediaObject** para que o objeto possa ser usado como um objeto de mídia do DirectX (DMO) e expõe a interface **IMFTransform** para que o objeto possa ser usado como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="091b3-227">A screen encoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="091b3-228">Um codificador de tela se comporta como DMO ou MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="091b3-228">A screen encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="091b3-229">A tabela a seguir mostra as condições sob as quais um codificador de tela se comporta como um DMO ou uma MFT.</span><span class="sxs-lookup"><span data-stu-id="091b3-229">The following table shows the conditions under which a screen encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="091b3-230">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="091b3-230">Operating system</span></span>            | <span data-ttu-id="091b3-231">Comportamento do codificador</span><span class="sxs-lookup"><span data-stu-id="091b3-231">Encoder behavior</span></span>                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="091b3-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="091b3-232">Windows XP</span></span>                  | <span data-ttu-id="091b3-233">Um codificador de tela do Windows Media sempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="091b3-233">A Windows Media Screen encoder always behaves as a DMO.</span></span>                                                                                             |
| <span data-ttu-id="091b3-234">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="091b3-234">Windows Vista and Windows 7</span></span> | <span data-ttu-id="091b3-235">Por padrão, um codificador de tela do Windows Media se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="091b3-235">By default, a Windows Media Screen encoder behaves as a DMO.</span></span> <span data-ttu-id="091b3-236">Se você obtiver uma interface **IMFTransform** em um codificador de tela, ela se comporta como um MFT.</span><span class="sxs-lookup"><span data-stu-id="091b3-236">If you obtain an **IMFTransform** interface on a screen encoder, it behaves as an MFT.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="091b3-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="091b3-237">Requirements</span></span>



| <span data-ttu-id="091b3-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="091b3-238">Requirement</span></span> | <span data-ttu-id="091b3-239">Valor</span><span class="sxs-lookup"><span data-stu-id="091b3-239">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="091b3-240">Cliente</span><span class="sxs-lookup"><span data-stu-id="091b3-240">Client</span></span><br/> | <span data-ttu-id="091b3-241">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="091b3-241">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="091b3-242">parâmetro</span><span class="sxs-lookup"><span data-stu-id="091b3-242">Header</span></span><br/> | <dl> <span data-ttu-id="091b3-243"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="091b3-243"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="091b3-244">DLL</span><span class="sxs-lookup"><span data-stu-id="091b3-244">DLL</span></span><br/>    | <dl> <span data-ttu-id="091b3-245"><dt>Wmvsencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="091b3-245"><dt>Wmvsencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="091b3-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="091b3-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="091b3-247">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="091b3-247">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="091b3-248">Implementação de codec</span><span class="sxs-lookup"><span data-stu-id="091b3-248">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="091b3-249">Usando o codec de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="091b3-249">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="091b3-250">Decodificador de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="091b3-250">Windows Media Video 9 Screen Decoder</span></span>](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




